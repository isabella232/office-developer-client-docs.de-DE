---
title: Implementieren eines Advise Sink-Objekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412107"
---
# <a name="implementing-an-advise-sink-object"></a>Implementieren eines Advise Sink-Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Client kann entweder eigene Advise Sink-Objekte implementieren oder eine Hilfsfunktion verwenden, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** erstellt ein advise sink-Objekt mit einer Implementierung von **OnNotify,** das eine Rückruffunktion aufruft. 
  
Die Verwendung von **HrAllocAdviseSink** hat Vor- und Nachteile. Es kann Arbeit speichern, aber es bietet keine Kontrolle über die Referenzzählung des von ihm erstellten Ratensenkenobjekts. Daher sollten Clients, die die Veröffentlichung ihrer Ratensenke sorgfältig steuern müssen oder die über Interabhängigkeiten zwischen derEntsprechungssenke und einem anderen Clientobjekt verfügen, eine eigene **IMAPIAdviseSink-Implementierung** erstellen und die Verwendung von **HrAllocAdviseSink** ganz vermeiden. 
  
Ein Client, der eine eigene Ratensenke implementieren soll, sollte ihn zu einem unabhängigen Objekt machen, das nicht mit anderen Objekten verwandt ist oder von diesen abhängig ist, um mögliche Komplikationen bei der Verweiszählung und Objektfreigabe zu vermeiden. Wenn Sie die Empfehlungssenke jedoch als Teil eines anderen Objekts implementieren oder einen Zurückzeiger auf ein anderes Objekt als Datenm member verwenden müssen, wird empfohlen, zwei separate Referenzanzahlen beizubehalten: eine für das Objekt, auf das von der Empfehlungssenke verwiesen wird, und eine für die Empfehlungssenke. 
  
Wenn die Referenzanzahl des referenzierten Objekts auf Null fällt, können alle methoden fehlschlagen und die vtable zerstört werden. Der Speicher für die Hinweissenke muss jedoch intakt bleiben, bis die Referenzanzahl ebenfalls auf Null fällt. Dies bedeutet, dass die **Release-Methode** der Hinweissenke ihre Referenzanzahl reduzieren und das Objekt zerstören muss, wenn diese Anzahl null erreicht. Wenn zwei separate Verweisanzahlen nicht beibehalten werden, ist es einfach, die Ratensenke im Rahmen des Release-Prozesses des umfassenden Objekts versehentlich **zu** zerstören. 
  
Clients, die **HrAllocAdviseSink** verwenden, um eine Ratensenke zu implementieren, müssen gleichermaßen darauf achten, ihre Rückruffunktion nicht als Methode in ein anderes Advise Sink-Objekt zu verwenden. Für C++-Clients ist es verlockend, dies zu tun und diesen Zeiger als Parameter zu übergeben.  Dies ist eine gefährliche Strategie, da Clients in der Regel ein Objekt frei machen, wenn die Referenzanzahl null erreicht. Wenn Sie den Arbeitsspeicher für das Objekt "Advise Sink" frei geben, würde dieser _Zeiger ungültig._ 
  
Je nach Ereignistyp und Ratenquelle kann Ihre **OnNotify-Methode** Ereignisse auf unterschiedliche Weise behandeln. In der folgenden Tabelle finden Sie Vorschläge zur Handhabung einiger Standardereignisse. 
  
|**Ereignistyp**|**Behandeln in OnNotify**|
|:-----|:-----|
|Objekt verschoben  <br/> |Wenn das ursprüngliche übergeordnete Objekt des verschobenen Objekts mit dem neuen übergeordneten Objekt verknüpft ist, aktualisieren Sie die Ansicht beginnend mit dem Ordner oder Adressbuchcontainer, der am höchsten in der Hierarchie ist. Wenn die beiden übergeordneten Container nichts miteinander zu tun haben, aktualisieren Sie beide Ansichten.  <br/> |
|Neue Nachricht  <br/> |Ändern Sie die Benutzeroberfläche, um den Benutzer über das Eintreffen einer oder mehreren neuen Nachrichten zu informieren. Platzieren Sie den Empfangsordner in der aktuellen Ansicht.  <br/> |
|Error  <br/> |Protokollieren Sie bei allen Objekten mit Ausnahme der Sitzung den Fehler, falls erforderlich, und geben Sie zurück. Melden Sie sich für das Sitzungsobjekt nach Möglichkeit ab.  <br/> |
|Suche abgeschlossen  <br/> |Keine Verarbeitung erforderlich.  <br/> |
   
> [!NOTE]
> Benachrichtigungshandler sollten erneut gesendet werden. 
  

