---
title: Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: In diesem Abschnitt werden die Dispatch-IDs für die Ereignisse beschrieben, die Outlook zur Verfügung stellt.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316877"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)

In diesem Abschnitt werden die Dispatch-IDs für die Ereignisse beschrieben, die Outlook zur Verfügung stellt.
  
Outlook macht die folgenden Dispatch-IDs (DispIds) verfügbar, damit C++-Add-Ins die entsprechenden Ereignisse über die [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) -Funktion abhören und behandeln können. 
  
|**Konstante**|**DISPID für Ereignis**|**Beschreibung**|**Parameter**|**Hinweise**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Wird verwendet, um das Ereignis auf Anwendungsebene aus der **IDispatch:: Invoke** -Funktion zu behandeln, die vor einem Druckvorgang ausgelöst wird.  <br/> | Es gibt zwei unbenannte Parameter:  <br/>  Der erste Parameter hat den Typ * * VT_BOOL|VT_BREF * *. Geben Sie **VARIANT_TRUE** in diesem Parameter zurück, um das Ereignis abzubrechen.  <br/>  Der zweite Parameter wird nicht verwendet und sollte ignoriert werden.  <br/> |Diese DISPID ist seit Outlook 2010 verfügbar.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Wird verwendet, um das Ereignis auf Elementebene aus der **IDispatch:: Invoke** -Funktion zu behandeln, die ausgelöst wird, wenn Outlook die Eigenschaften des Elements gelesen hat.  <br/> |Es gibt nur einen Parameter _Cancel_ , der vom Typ * * VT_BOOL|VT_BREF * *. Geben Sie **VARIANT_TRUE** in diesem Parameter zurück, um den Lesevorgang abzubrechen.  <br/> |Diese DISPID ist seit Outlook 2010 verfügbar.  <br/> Dieses Ereignis entspricht dem Ereignis **IExchExtMessageEvents:: OnReadComplete**für Exchange-Client Erweiterungen (ECE) und auch dem **ReadComplete** -Ereignis, das dem objektmodell seit Outlook 2013 hinzugefügt wurde.  <br/> |
   
Ein Beispiel für die Verwendung einer DispID zum Abhören und behandeln eines Ereignisses finden Sie in der in `CAppEventListener::Invoke` [Implementieren von Outlook 2002/XP-Ereignissenken in MFC c++ 2003 .net](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)beschriebenen Funktion in der c++-Outlook-Lösung.
  
## <a name="see-also"></a>Siehe auch

- [Aus Outlook exportierte APIs](outlook-exported-apis.md)
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Informationen zu von Outlook exportierten APIs](about-apis-exported-by-outlook.md)
- [Implementieren von Outlook 2002/XP-Ereignissenken in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

