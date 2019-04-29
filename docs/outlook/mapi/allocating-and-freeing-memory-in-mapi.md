---
title: Reservieren und Freigeben von Arbeitsspeicher in MAPI
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
# <a name="allocating-and-freeing-memory-in-mapi"></a>Reservieren und Freigeben von Arbeitsspeicher in MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zur Angabe, wie Arbeitsspeicher reserviert und freigegeben werden soll, definiert MAPI ein Modell, um zu wissen, wann der zwischen Public Interface Method und API-Funktionsaufruf übergebene Speicher freigegeben werden soll. Das Modell gilt nur für Arbeitsspeicher, der für Parameter reserviert ist, die keine Zeiger auf Schnittstellen sind, wie Zeichenfolgen und Zeiger auf Strukturen. Schnittstellenzeiger verwenden den Verweis Zählmechanismus, der über **IUnknown**implementiert wird. Wenn Sie nicht-MAPI-bezogenen Speicher intern innerhalb einer Clientanwendung oder eines Dienstanbieters zuweisen und freigeben, verwenden Sie, was sinnvoll ist. 
  
Das Modell definiert Parameter als einen von drei Typen. Sie können Eingabeparameter sein, die vom Aufrufer mit Informationen festgelegt werden, die von der aufgerufenen Funktion oder Methode verwendet werden, Ausgabeparameter, die von der aufgerufenen Funktion oder Methode festgelegt und an den Aufrufer zurückgegeben werden, oder Eingabe-Ausgabeparameter, eine Kombination der beiden Typen. Ausgabeparameter sind häufig Zeiger auf Daten oder Zeiger auf Zeiger auf Daten. Obwohl die aufgerufene Funktion für die Zuordnung der Daten für Ausgabeparameter zuständig ist, weist der Aufrufer den Arbeitsspeicher für den Zeiger zu. 
  
In der folgenden Tabelle werden die Regeln für die Zuordnung und Freigabe von Arbeitsspeicher für diese Typen von Parametern erläutert.
  
|**Type**|**Speicherzuordnung**|**Speicherfreigabe**|
|:-----|:-----|:-----|
|Input  <br/> |Der Anrufer ist verantwortlich und kann einen beliebigen Mechanismus verwenden.  <br/> |Der Anrufer ist verantwortlich und kann einen beliebigen Mechanismus verwenden.  <br/> |
|Output  <br/> |Die aufgerufene Funktion ist verantwortlich und muss **MAPIAllocateBuffer**verwenden. Weitere Informationen finden Sie unter [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Der Anrufer ist verantwortlich und muss **mapifreebufferfreigegeben**verwenden. Weitere Informationen finden Sie unter [mapifreebufferfreigegeben](mapifreebuffer.md).  <br/> |
|Input-Output  <br/> |Der Aufrufer ist für die anfängliche Zuordnung verantwortlich, und die aufgerufene Funktion kann bei Bedarf mithilfe von **MAPIAllocateBuffer**neu zugewiesen werden.  <br/> |Die aufgerufene Funktion ist für die anfängliche Freigabe verantwortlich, wenn eine Neuzuordnung erforderlich ist. Der Anrufer muss den endgültigen Rückgabewert freigeben.  <br/> |
   
Bei Fehlerbedingungen müssen Implementierer der Schnittstellenmethoden auf Ausgabe-und Eingabe Ausgabeparameter achten, da der Aufrufer im Allgemeinen keine Möglichkeit hat, Sie zu bereinigen. Wenn ein Fehler zurückgegeben wird, muss jeder Output-oder Input-Output-Parameter entweder auf den vom Aufrufer initialisierten Wert oder auf einen Wert festgelegt werden, der ohne Aktion des Anrufers bereinigt werden kann. Beispielsweise muss ein Ausgabezeiger-Parameter von `void ** ppv` wie bei der Eingabe bleiben, oder er kann auf NULL ( `*ppv = NULL`) festgelegt werden.
  

