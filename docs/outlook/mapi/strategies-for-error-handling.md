---
title: Strategien für die Fehlerbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9e76ae3f292d8348b9dc64cb54bffae96b96e871
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424147"
---
# <a name="strategies-for-error-handling"></a>Strategien für die Fehlerbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da Schnittstellenmethoden virtuell sind, ist es nicht möglich, als Aufrufer den vollständigen Satz von Werten zu kennen, die von einem beliebigen Aufruf zurückgegeben werden können. Eine Implementierung einer Methode kann fünf Werte zurückgeben. Ein anderer kann acht zurückgeben. Die Referenzeinträge in der #A0 enthalten einige Werte, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Ihr Client oder Dienstanbieter überprüfen und behandeln kann, da sie besondere Bedeutungen haben. Andere Werte können zurückgegeben werden, aber da sie nicht aussagekräftig sind, ist spezieller Code zur Verarbeitung dieser Werte nicht erforderlich. Eine einfache Überprüfung auf Erfolg oder Fehler ist ausreichend.
  
Einige der Schnittstellenmethoden geben Warnungen zurück. Wenn eine Methode, die Ihr Client oder Dienstanbieter  aufruft, eine Warnung zurückgeben kann, verwenden Sie das HR_FAILED-Makro, um den Rückgabewert zu testen, anstatt auf Null oder ungleich Null zu überprüfen. Warnungen unterscheiden sich, obwohl ungleich Null, von Fehlercodes, da sie nicht über den hohen Bitsatz verfügen. Wenn Ihr Client oder Dienstanbieter das Makro nicht verwendet, ist es wahrscheinlich, dass eine Warnung mit einem Fehler irrt. 
  
Obwohl die meisten Schnittstellenmethoden und -funktionen HRESULT-Werte zurückgeben, geben einige Funktionen nicht signierte lange Werte zurück. Außerdem stammen einige methoden, die in der MAPI-Umgebung verwendet werden, aus COM und geben COM-Fehlerwerte anstelle von MAPI-Fehlerwerten zurück. Beachten Sie beim Telefonieren die folgenden Richtlinien:
  
- Verwenden Sie niemals die Rückgabewerte von **IUnknown::AddRef** oder **IUnknown::Release.** Diese Rückgabewerte dienen nur zu Diagnosezwecken. 
    
- **IUnknown::QueryInterface** gibt immer generische COM-Fehler zurück, bei denen die Einrichtung FACILITY_NULL oder FACILITY_RPC anstelle von MAPI-Fehlern ist. 
    
- Alle anderen Schnittstellenmethoden geben MAPI-Schnittstellenfehler mit einer Möglichkeit von FACILITY_ITF oder FACILITY_RPC oder FACILITY_NULL zurück.
    
Wenn ein Aufruf einer nicht unterstützten MAPI-Methode erfolgt, kann einer von vier möglichen Fehlern zurückgegeben werden: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

