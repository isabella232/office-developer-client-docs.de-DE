---
title: Implementieren einer Advise-Empfängerobjekt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a95222f8ec75c519558636cf54111f28cbe14066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792551"
---
# <a name="implementing-an-advise-sink-object"></a>Implementieren einer Advise-Empfängerobjekt

  
  
**Betrifft**: Outlook 
  
Ein Client kann entweder Implementieren der Empfängerobjekten eigene Advise oder eine Hilfsfunktion [HrAllocAdviseSink](hrallocadvisesink.md)verwenden. **HrAllocAdviseSink** erstellt ein Advise-Empfänger-Objekt mit einer Implementierung der **OnNotify** , die eine Callback-Funktion aufruft. 
  
Vor- und Nachteile der Verwendung von **HrAllocAdviseSink**sind. Sie können Arbeit speichern, aber es bietet keine Kontrolle über Verweis zählen von der Advise-Empfängerobjekt, das erstellt wird. Aus diesem Grund sollten Clients, die ihre Advise-Empfänger Version sorgfältig kontrollieren möchten, oder deren Abhängigkeiten zwischen ihren Advise-Empfänger und einem anderen Clientobjekt, Erstellen ihrer eigenen **IMAPIAdviseSink** -Implementierung und vermeiden der Verwendung von ** HrAllocAdviseSink** vollständig. 
  
Ein Client, implementieren eine eigene Advise-Empfänger sollte ein unabhängiger-Objekt nicht im Zusammenhang mit der oder alle anderen Objekte Allgemein Komplikationen in Verweis-Zählvorgängen und Objekt Version zu vermeiden abhängenden ermöglichen. Jedoch, wenn Sie müssen Advise-Empfänger im Rahmen eines anderen Objekts implementieren oder einen Back Zeiger in ein anderes Objekt als Datenmember einschließen, es wird empfohlen, dass zwei separate Referenzzähler verwaltet werden: eine für das Objekt, die durch die Advise-Empfänger und einen für die Advise-Empfänger. 
  
Wenn die Anzahl der Verweise des referenzierten Objekts 0 (null) liegt, alle ihre Methoden kann fehlschlagen und die vtable des Objekts kann gelöscht werden, aber des Speichers für die Advise-Empfänger muss erst nach seiner Referenzzähler auch auf 0 (null) fällt bleiben. Dies bedeutet, dass der Advise-Empfänger **Release** -Methode muss den Referenzzähler verringert und Fertig stellen, das Objekt löschen, wenn diese Anzahl 0 (null) erreicht. Wenn zwei separate Referenzzähler nicht verwaltet werden, wäre es leicht zu Advise-Empfänger als Teil **des Objekts übergreifende Freigabeprozess** versehentlich gelöscht. 
  
Clients verwenden **HrAllocAdviseSink** Advise-Empfänger implementieren müssen gleichmäßig auf keinen Fall ihre Callback-Funktion als eine Methode in einer anderen Advise-Empfängerobjekt enthalten sein. C++-Clients ist es läge vertraut sind, und den _diesem_ Zeiger als Parameter übergeben. Dies ist eine gefährlicher Strategie, da Clients in der Regel ein Objekt frei, wenn seine Referenzzähler 0 (null) erreicht. Freigeben des Speichers für das Empfängerobjekt Advise würden _diese_ den Zeiger ungültig wird. 
  
Je nach Typ des Ereignisses und die Advise-Quelle kann Ihre **OnNotify** -Methode auf verschiedene Weise behandeln. In der folgenden Tabelle wird das in einige der Standardereignisse Behandlung von Vorschlägen. 
  
|**Ereignistyp**|**Behandeln von OnNotify**|
|:-----|:-----|
|Objekt wurde verschoben  <br/> |Wenn das verschobene ursprüngliche übergeordnete Objekt für das neue übergeordnete Element verknüpft ist, aktualisieren Sie am Anfang der Ansicht mit dem Ordner oder Adressbuchcontainer in der Hierarchie. Wenn die zwei übergeordneten Container nicht miteinander verknüpft sind, aktualisieren Sie beide den Ansichten.  <br/> |
|Neue Nachricht  <br/> |Ändern der Benutzeroberfläche, um den Benutzer über den Empfang von einen oder mehrere neue Nachrichten zu informieren. Platzieren Sie den Empfangsordner in der aktuellen Ansicht.  <br/> |
|Fehler  <br/> |Melden Sie für alle Objekte außer der Sitzung den Fehler bei Bedarf und zurück. Melden Sie für das Sitzungsobjekt Wenn möglich ab.  <br/> |
|Suche abgeschlossen  <br/> |Keine Verarbeitung erforderlich.  <br/> |
   
> [!NOTE]
> Benachrichtigungshandler sollte wiedereintretende sein. 
  

