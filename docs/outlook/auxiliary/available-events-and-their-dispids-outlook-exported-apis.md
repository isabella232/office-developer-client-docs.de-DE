---
title: Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1fd848c7-038e-4e2f-8997-c8509b31df79
description: Dieser Abschnitt beschreibt die Versendung Bezeichner für die Ereignisse, die Outlook verfügbar gemacht werden.
ms.openlocfilehash: 31843a2eb8f91eabdc0dbf54a269270eb172baa7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400236"
---
# <a name="available-events-and-their-dispids-outlook-exported-apis"></a>Verfügbaren Ereignisse und ihrer Dispids (Outlook exportierter APIs)

Dieser Abschnitt beschreibt die Versendung Bezeichner für die Ereignisse, die Outlook verfügbar gemacht werden.
  
Outlook macht die folgenden Versendung-IDs (Dispids) um C++-add-ins zum Abhören von und behandeln die entsprechenden Ereignisse aus der [IDispatch:: Invoke](https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke) -Funktion zu ermöglichen. 
  
|**Konstante**|**DISPID für-Ereignis**|**Beschreibung**|**Parameter**|**Hinweise**|
|:-----|:-----|:-----|:-----|:-----|
|**dispidBeforePrint** <br/> |0xFC8E  <br/> |Verwendet, um das Ereignis auf Anwendungsebene aus der **IDispatch:: Invoke** -Funktion zu behandeln, die vor einem Druckvorgang ausgelöst.  <br/> | Es gibt 2 unbenannte Parameter:  <br/>  Der erste Parameter des Typs ist ** VT_BOOL|VT_BREF **. Geben Sie in diesem Parameter wird das Ereignis abgebrochen **VARIANT_TRUE** zurück.  <br/>  Der zweite Parameter wird nicht verwendet und sollte ignoriert werden.  <br/> |Diese Dispid ist ab Outlook 2010 verfügbar.  <br/> |
|**dispidEventReadComplete** <br/> |0xFC8F  <br/> |Verwendet, um das Ereignis Elementebene die **IDispatch:: Invoke** -Funktion zu behandeln, das ausgelöst wird, wenn Outlook abgeschlossen ist, lesen die Eigenschaften des Elements.  <br/> |Es gibt nur einen Parameter vom Typ ist _Abbrechen_ ** VT_BOOL|VT_BREF **. Geben Sie in diesem Parameter lesen-Vorgang Abbrechen **VARIANT_TRUE** zurück.  <br/> |Diese Dispid ist ab Outlook 2010 verfügbar.  <br/> Dieses Ereignis entspricht dem Exchange Client Extensions (ECE)-Ereignis **IExchExtMessageEvents::OnReadComplete**, und auch auf die **"ReadComplete** "-Ereignis hinzugefügt wurde auf das Objektmodell seit Outlook 2013.  <br/> |
   
Ein Beispiel dafür, wie Sie mit einer Dispid anhören und Verarbeiten eines Ereignisses, finden Sie unter der `CAppEventListener::Invoke` -Funktion in der C++-Outlook-Lösung in der [Implementierung von Outlook 2002/XP Ereignissenken in MFC C++ 2003 .NET](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)beschrieben.
  
## <a name="see-also"></a>Siehe auch

- [Aus Outlook exportierte APIs](outlook-exported-apis.md)
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Informationen zu von Outlook exportierten APIs](about-apis-exported-by-outlook.md)
- [Implementieren von Outlook 2002/XP-Ereignis in MFC C++ 2003 .NET senken](https://www.codeproject.com/Articles/4230/Implementing-Outlook-2002-XP-Event-Sinks-in-MFC-C)

