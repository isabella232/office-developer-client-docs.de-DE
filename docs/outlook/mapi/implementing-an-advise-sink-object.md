---
title: Implementieren eines Advise-Senke-Objekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351100"
---
# <a name="implementing-an-advise-sink-object"></a>Implementieren eines Advise-Senke-Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann entweder eigene Advise-Empfängerobjekte implementieren oder eine Hilfsfunktion [HrAllocAdviseSink](hrallocadvisesink.md)verwenden. **HrAllocAdviseSink** erstellt ein Advise-Senke-Objekt mit **** einer Implementierung von OnNotify, die eine Rückruffunktion aufruft. 
  
Es gibt vor-und Nachteile bei der Verwendung von **HrAllocAdviseSink**. Es kann Arbeit speichern, aber es bietet keine Kontrolle über die Verweiszählung des Advise-Senke-Objekts, das es erstellt. Daher sollten Clients, die die Freigabe ihrer Advise-Senke sorgfältig steuern müssen oder die gegenseitige Abhängigkeiten zwischen Ihrer Advise-Senke und einem anderen Clientobjekt aufweisen, ihre eigene **IMAPIAdviseSink** -Implementierung erstellen und die Verwendung **von HrAllocAdviseSink** . 
  
Ein Client, der seine eigene Advise-Senke implementiert, sollte es zu einem unabhängigen Objekt machen, das nicht mit oder von anderen Objekten abhängig ist, um mögliche Komplikationen bei der Verweiszählung und der Objektfreigabe zu vermeiden. Wenn Sie jedoch ihre Advise-Senke als Teil eines anderen Objekts implementieren oder einen Rückzeiger auf ein anderes Objekt als Datenmember einfügen müssen, wird empfohlen, zwei getrennte Verweiszähler beizubehalten: eine für das Objekt, auf das von der Advise-Senke verwiesen wird, und eine für die Advise-Senke. 
  
Wenn der Verweiszähler des referenzierten Objekts auf 0 (null) fällt, können alle seine Methoden fehlschlagen und seine Vtable kann zerstört werden, aber der Speicher für die Advise-Senke muss intakt bleiben, bis der Verweiszähler auch auf Null fällt. Dies hat zur Folge, dass die **Release** -Methode der Advise-Senke den Verweiszähler verringern und das Objekt zerstören muss, wenn diese Anzahl Null erreicht. Wenn zwei getrennte Verweiszähler nicht verwaltet werden, wäre es einfach, die Advise-Senke als Teil des **Release** -Prozesses des umfassenden Objekts versehentlich zu zerstören. 
  
Clients, die **HrAllocAdviseSink** zum Implementieren einer Advise-Senke verwenden, müssen ebenso darauf achten, dass Sie Ihre Rückruffunktion nicht als Methode in einem anderen Advise-Senke-Objekt einbeziehen. Für C++-Clients ist es verlockend, dies zu tun und den _this_ -Zeiger als Parameter zu übergeben. Dies ist eine gefährliche Strategie, da Clients in der Regel ein Objekt freigeben, wenn der Verweiszähler Null erreicht. Durch Freigeben des Speichers für das Advise-Senke-Objekt würde _dieser_ Zeiger ungültig. 
  
Je nach Art des Ereignisses und der Advise-Quelle kann die **OnNotify** -Methode Ereignisse auf unterschiedliche Weise behandeln. In der folgenden Tabelle finden Sie Vorschläge, wie Sie einige der Standardereignisse behandeln können. 
  
|**Ereignistyp**|**Behandlung in onNotify**|
|:-----|:-----|
|Objekt verschoben  <br/> |Wenn das ursprüngliche übergeordnete Objekt des verschobenen Objekts mit dem neuen übergeordneten Element verknüpft ist, aktualisieren Sie die Ansicht, beginnend mit dem Ordner-oder Adressbuchcontainer am höchsten in der Hierarchie. Wenn die beiden übergeordneten Container nicht miteinander verbunden sind, aktualisieren Sie beide Ansichten.  <br/> |
|Neue Nachricht  <br/> |Ändern Sie die Benutzeroberfläche, um den Benutzer über das Eintreffen einer oder mehrerer neuer Nachrichten zu informieren. Platzieren Sie den Empfangsordner in der aktuellen Ansicht.  <br/> |
|Fehler  <br/> |Protokollieren Sie bei allen Objekten mit Ausnahme der Sitzung den Fehler, falls erforderlich, und geben Sie zurück. Melden Sie sich bei dem Session-Objekt ab, falls möglich.  <br/> |
|Vollständige Suche  <br/> |Keine Verarbeitung erforderlich.  <br/> |
   
> [!NOTE]
> Benachrichtigungshandler sollten wieder eintreten. 
  

