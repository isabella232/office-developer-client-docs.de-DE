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
ms.openlocfilehash: 2ec5c2604c72d41078aa467764463e2659c62e65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587943"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Reservieren und Freigeben von Arbeitsspeicher in MAPI

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Zusätzlich zum angeben, wie zuordnen und Freigeben von Arbeitsspeicher, definiert MAPI ein Modell zu wissen, wenn Speicher übergeben zwischen öffentliche Schnittstelle-Methode und die API-Funktion, die Anrufe freigegeben werden soll. Das Modell gilt nur für Arbeitsspeichers für Parameter, die nicht Zeigern auf Schnittstellen, wie Zeichenfolgen und Zeiger auf Strukturen sind. Schnittstellenzeiger verwenden Sie die Referenz zählen Mechanismus über **IUnknown**implementiert. Verwenden Sie beim Zuordnen und Freigeben von nicht-MAPI-Speicher intern innerhalb einer Clientanwendung oder -Dienstanbieter verbunden, geeigneter Mechanismus sinnvoll ist. 
  
Das Modell definiert Parameter als eine der drei Typen. Sie können Eingaben werden Parameter, festgelegt vom Anrufer mit Informationen, die von der aufgerufenen Funktion oder Methode verwendet werden Ausgabeparameter, von der aufgerufenen Funktion oder Methode festgelegt und an den Anrufer oder Input-Output-Parameter, eine Kombination aus den beiden Typen zurückgegeben. Ausgabeparameter sind häufig Zeiger auf Daten oder Zeiger auf Zeiger auf Daten. Obwohl die aufgerufene Funktion zur Zuweisung von Daten für Ausgabeparameter zuständig ist, weist der Anrufer den Speicher für den Zeiger. 
  
In der folgenden Tabelle werden die Regeln für das zuordnen und Freigeben von Arbeitsspeicher für diese Typen von Parametern erläutert.
  
|**Typ**|**Zuweisung von virtuellem Speicher**|**Arbeitsspeicher-Version**|
|:-----|:-----|:-----|
|Eingabe  <br/> |Anrufer ist dafür verantwortlich, und einen Mechanismus verwenden kann.  <br/> |Anrufer ist dafür verantwortlich, und einen Mechanismus verwenden kann.  <br/> |
|Ausgabe  <br/> |Aufgerufene Funktion ist dafür verantwortlich, und muss **MAPIAllocateBuffer**verwenden. Weitere Informationen finden Sie unter [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Anrufer ist dafür verantwortlich, und muss **MAPIFreeBuffer**verwenden. Weitere Informationen finden Sie unter [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Ein-/ Ausgabe  <br/> |Anrufer ist verantwortlich für die ursprüngliche Zuordnung und aufgerufene Funktion bei Bedarf neu zuordnen können **MAPIAllocateBuffer**verwenden.  <br/> |Aufgerufene Funktion ist verantwortlich für die anfängliche freigeben, wenn Neubelegung notwendig wird. Anrufer muss den letzten Rückgabewert frei.  <br/> |
   
Während der fehlerbedingungen müssen Implementierer Schnittstellenmethoden, da der Aufrufer im Allgemeinen keine Möglichkeit hat, diese zu bereinigen Ausgabe und Input Output-Parameter achten. Wenn ein Fehler zurückgegeben wird, darf klicken Sie dann jede Ausgabe oder Input Output-Parameter entweder gelassen werden am Wert initialisiert vom Anrufer oder einen Wert, die ohne alle Unternehmensbereiche der Aufrufer bereinigt werden können. Beispielsweise einen Zeiger-Ausgabeparameter des `void ** ppv` muss bleiben, wie sie bei der Eingabe wurde oder auf NULL festgelegt werden kann ( `*ppv = NULL`).
  

