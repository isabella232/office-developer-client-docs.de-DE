---
title: Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: In diesem Abschnitt werden die Verteilerbezeichner für die Ereignisse beschrieben, die Outlook zur Verfügung stellt.
ms.openlocfilehash: d226fa92e96fea9092990b7c5ee290ce2df2cdaf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568082"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)

In diesem Abschnitt werden die Verteilerbezeichner für die Ereignisse beschrieben, die Outlook zur Verfügung stellt.
  
Outlook macht die folgenden Verteiler-IDs (Dispids) verfügbar, damit C++-Add-Ins die entsprechenden Ereignisse aus der [IDispatch::Invoke-Funktion](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) abhören und behandeln können. 
  
|**Konstante**|**Dispid für Ereignis**|**Beschreibung**|**Parameter**|**Bemerkungen**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Wird verwendet, um das Ereignis auf Anwendungsebene aus der **IDispatch::Invoke-Funktion** zu behandeln, die vor einem Druckvorgang ausgelöst wird.  <br/> | Es gibt 2 unbenannte Parameter:  <br/>  Der erste Parameter ist vom Typ **VT_BOOL|VT_BREF**. Geben Sie **VARIANT_TRUE** in diesem Parameter zurück, um das Ereignis abzubrechen.  <br/>  Der zweite Parameter wird nicht verwendet und sollte ignoriert werden.  <br/> |Diese Dispid ist seit Outlook 2010 verfügbar.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Wird verwendet, um das Ereignis auf Elementebene aus der **IDispatch::Invoke-Funktion** zu behandeln, die ausgelöst wird, wenn Outlook das Lesen der Eigenschaften des Elements abgeschlossen hat.  <br/> |Es gibt nur einen Parameter  _"Cancel",_ der vom Typ **VT_BOOL|VT_BREF**. Geben Sie **VARIANT_TRUE** in diesem Parameter zurück, um den Lesevorgang abzubrechen.  <br/> |Diese Dispid ist seit Outlook 2010 verfügbar.  <br/> Dieses Ereignis entspricht dem Exchange Client Extensions (ECE)-Ereignis **IExchExtMessageEvents::OnReadComplete** und auch dem **ReadComplete-Ereignis,** das dem Objektmodell seit Outlook 2013 hinzugefügt wurde.  <br/> |
   
Ein Beispiel für die Verwendung einer Dispid zum Überwachen und Behandeln eines Ereignisses finden Sie in der `CAppEventListener::Invoke` Funktion in der C++-Outlook Lösung, die unter [Implementieren von Outlook 2002/XP-Ereignissenken in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)beschrieben ist.
  
## <a name="see-also"></a>Siehe auch

- [Aus Outlook exportierte APIs](outlook-exported-apis.md)
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Informationen zu von Outlook exportierten APIs](about-apis-exported-by-outlook.md)
- [Implementieren von Outlook 2002/XP-Ereignissenken in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

