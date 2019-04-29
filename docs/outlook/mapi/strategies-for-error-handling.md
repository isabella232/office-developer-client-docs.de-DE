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
  
Da Schnittstellenmethoden virtuell sind, ist es nicht möglich, als Anrufer den vollständigen Satz von Werten zu kennen, die von einem beliebigen Aufruf zurückgegeben werden können. Eine Implementierung einer Methode kann fünf Werte zurückgeben. eine andere kann acht zurückgeben. In den Referenz Einträgen in der MAPI-Dokumentation werden einige Werte aufgeführt, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Ihr Client oder Dienstanbieter überprüfen und behandeln kann, da diese eine besondere Bedeutung haben. Andere Werte können zurückgegeben werden, da Sie jedoch keine Bedeutung haben, ist kein spezieller Code erforderlich, um diese zu behandeln. Eine einfache Überprüfung auf Erfolg oder Misserfolg ist ausreichend.
  
Einige der Schnittstellenmethoden geben Warnungen zurück. Wenn eine vom Client oder Dienstanbieter aufgerufene Methode eine Warnung zurückgeben kann, verwenden Sie das **HR_FAILED** -Makro, um den Rückgabewert zu testen, statt eine Überprüfung auf 0 (null) oder ungleich NULL. Warnungen, obwohl ungleich NULL, unterscheiden sich von Fehlercodes dadurch, dass Sie nicht das hohe Bit festgelegt haben. Wenn Ihr Client oder Dienstanbieter das Makro nicht verwendet, ist es wahrscheinlich, dass für einen Fehler eine Warnung verwechselt wird. 
  
Obwohl die meisten Schnittstellenmethoden und-Funktionen HRESULT-Werte zurückgeben, geben einige Funktionen unsigned long-Werte zurück. Außerdem stammen einige Methoden, die in der MAPI-Umgebung verwendet werden, aus COM und geben COM-Fehlerwerte anstelle von MAPI-Fehlerwerten zurück. Beachten Sie beim tätigen von Anrufen die folgenden Richtlinien:
  
- Verlassen Sie sich nie auf die Rückgabewerte von **IUnknown:: AddRef** oder **IUnknown:: Release**. Diese Rückgabewerte dienen nur zu Diagnosezwecken. 
    
- **IUnknown:: QueryInterface** gibt immer generische com-Fehler zurück, bei denen die FACILITY_NULL-oder FACILITY_RPC statt MAPI-Fehler aufweist. 
    
- Alle anderen Schnittstellenmethoden geben MAPI-Schnittstellenfehler mit einer FACILITY_ITF-oder FACILITY_RPC-oder FACILITY_NULL-Fehlermeldung zurück.
    
Wenn ein Aufruf an eine nicht unterstützte MAPI-Methode erfolgt, kann einer von vier möglichen Fehlern zurückgegeben werden: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

