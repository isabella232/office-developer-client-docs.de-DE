---
title: Zuordnen und Freigeben von Arbeitsspeicher in MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5a0d6dd27d36c6631e5a66e522fb1f0fe6223e11
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567865"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Zuordnen und Freigeben von Arbeitsspeicher in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zur Angabe, wie Speicher zugeordnet und freigegeben werden soll, definiert MAPI ein Modell, um zu wissen, wann zwischen öffentlichen Schnittstellenmethoden und API-Funktionsaufrufen übergebener Speicher freigegeben werden soll. Das Modell gilt nur für Speicher, der für Parameter reserviert ist, die keine Zeiger auf Schnittstellen sind, z. B. Zeichenfolgen und Zeiger auf Strukturen. Schnittstellenzeiger verwenden den Referenzzählungsmechanismus, der über **IUnknown** implementiert wird. Verwenden Sie bei der internen Zuweisung und Freigabe von Nicht-MAPI-bezogenen Speicher innerhalb einer Clientanwendung oder eines Dienstanbieters den sinnvollen Mechanismus. 
  
Das Modell definiert Parameter als einen von drei Typen. Sie können Eingabeparameter sein, die vom Aufrufer mit Informationen festgelegt werden, die von der aufgerufenen Funktion oder Methode verwendet werden sollen, Ausgabeparameter, die von der aufgerufenen Funktion oder Methode festgelegt und an den Aufrufer zurückgegeben werden, oder Eingabeausgabeparameter, eine Kombination der beiden Typen. Ausgabeparameter sind häufig Zeiger auf Daten oder Zeiger auf Datenzeiger. Obwohl die aufgerufene Funktion für die Zuweisung der Daten für Ausgabeparameter zuständig ist, weist der Aufrufer den Speicher für den Zeiger zu. 
  
Die Regeln für die Zuweisung und Freigabe von Arbeitsspeicher für diese Parametertypen werden in der folgenden Tabelle erläutert.
  
|**Typ**|**Speicherzuordnung**|**Speicherfreigabe**|
|:-----|:-----|:-----|
|Input  <br/> |Der Anrufer ist verantwortlich und kann jeden Mechanismus verwenden.  <br/> |Der Anrufer ist verantwortlich und kann jeden Mechanismus verwenden.  <br/> |
|Ausgabe  <br/> |Die aufgerufene Funktion ist verantwortlich und muss **MAPIAllocateBuffer** verwenden. Weitere Informationen finden Sie unter [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Der Aufrufer ist verantwortlich und muss **MAPIFreeBuffer** verwenden. Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Eingabeausgabe  <br/> |Der Aufrufer ist für die anfängliche Zuordnung verantwortlich, und die aufgerufene Funktion kann bei Bedarf mit **MAPIAllocateBuffer** neu zugeordnet werden.  <br/> |Die aufgerufene Funktion ist für die anfängliche Freigabe verantwortlich, wenn eine Neuzuweisung erforderlich ist. Der Aufrufer muss den endgültigen Rückgabewert freigeben.  <br/> |
   
Bei Fehlerbedingungen müssen Implementierer von Schnittstellenmethoden auf Ausgabe- und Eingabeausgabeparameter achten, da der Aufrufer diese im Allgemeinen nicht bereinigen kann. Wenn ein Fehler zurückgegeben wird, muss jeder Ausgabe- oder Eingabeausgabeparameter entweder auf dem vom Aufrufer initialisierten Wert belassen oder auf einen Wert festgelegt werden, der ohne Aktion des Aufrufers bereinigt werden kann. Ein Ausgabezeigerparameter von muss beispielsweise  `void ** ppv` so belassen werden, wie er bei der Eingabe war, oder kann auf NULL ( ) festgelegt  `*ppv = NULL` werden.
  

