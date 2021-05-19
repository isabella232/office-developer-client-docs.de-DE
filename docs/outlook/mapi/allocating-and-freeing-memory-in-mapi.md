---
title: Zuordnen und Freispeichern in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419667"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Zuordnen und Freispeichern in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Neben der Angabe, wie Arbeitsspeicher zugewiesen und frei gemacht werden soll, definiert MAPI ein Modell, um zu wissen, wann der zwischen methoden der öffentlichen Schnittstelle und API-Funktionsaufrufen übergebene Arbeitsspeicher frei werden soll. Das Modell gilt nur für Denkspeicher, der für Parameter reserviert ist, die keine Zeiger auf Schnittstellen sind, z. B. Zeichenfolgen und Zeiger auf Strukturen. Schnittstellenzeiger verwenden den Referenzzählmechanismus, der über **IUnknown implementiert wurde.** Verwenden Sie beim Zuweisen und Freispeichern von nicht MAPI-bezogenen Arbeitsspeicher intern innerhalb einer Clientanwendung oder eines Dienstanbieters jeden Mechanismus, der sinnvoll ist. 
  
Das Modell definiert Parameter als einen von drei Typen. Dies können Eingabeparameter sein, die vom Aufrufer mit Informationen festgelegt werden, die von der aufgerufenen Funktion oder Methode verwendet werden sollen, Ausgabeparameter, die von der aufgerufenen Funktion oder Methode festgelegt und an den Aufrufer zurückgegeben werden, oder Eingabeausgabeparameter, eine Kombination der beiden Typen. Ausgabeparameter sind häufig Zeiger auf Daten oder Zeiger auf Zeiger auf Daten. Obwohl die aufgerufene Funktion für die Zuordnung der Daten für Ausgabeparameter verantwortlich ist, weist der Aufrufer den Arbeitsspeicher für den Zeiger zu. 
  
Die Regeln zum Zuordnen und Freigeben von Arbeitsspeicher für diese Parametertypen werden in der folgenden Tabelle erläutert.
  
|**Typ**|**Speicherzuordnung**|**Speicherversion**|
|:-----|:-----|:-----|
|Input  <br/> |Der Anrufer ist verantwortlich und kann einen beliebigen Mechanismus verwenden.  <br/> |Der Anrufer ist verantwortlich und kann einen beliebigen Mechanismus verwenden.  <br/> |
|Ausgabe  <br/> |Die aufgerufene Funktion ist verantwortlich und muss **MAPIAllocateBuffer verwenden.** Weitere Informationen finden Sie unter [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Der Anrufer ist verantwortlich und muss **MAPIFreeBuffer verwenden.** Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Eingabeausgabe  <br/> |Der Aufrufer ist für die anfängliche Zuordnung verantwortlich, und die aufgerufene Funktion kann bei Bedarf mithilfe von **MAPIAllocateBuffer neu zugeordnet werden.**  <br/> |Die aufgerufene Funktion ist für die anfängliche Freilegung verantwortlich, wenn eine Neuzuordnung erforderlich ist. Der Anrufer muss den endgültigen Rückgabewert frei geben.  <br/> |
   
Bei Ausfallbedingungen müssen Implementierer von Schnittstellenmethoden auf Ausgabe- und Eingabeausgabeparameter achten, da der Aufrufer in der Regel keine Möglichkeit hat, sie zu bereinigen. Wenn ein Fehler zurückgegeben wird, muss jeder Ausgabe- oder Eingabeausgabeparameter entweder am vom Aufrufer initialisierten Wert bleiben oder auf einen Wert festgelegt werden, der ohne Aktion des Aufrufers bereinigt werden kann. Beispielsweise muss ein Ausgabezeigerparameter von wie bei der Eingabe links bleiben  `void ** ppv` oder auf NULL ( ) festgelegt  `*ppv = NULL` werden.
  

