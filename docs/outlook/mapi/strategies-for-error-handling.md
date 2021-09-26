---
title: Strategien für die Fehlerbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 73222ba42fa0e46316f01534340a8194abf674a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591038"
---
# <a name="strategies-for-error-handling"></a>Strategien für die Fehlerbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Da Schnittstellenmethoden virtuell sind, ist es nicht möglich, als Aufrufer den vollständigen Wertesatz zu kennen, der von einem aufruf zurückgegeben werden kann. Eine Implementierung einer Methode kann fünf Werte zurückgeben. eine andere gibt möglicherweise acht zurück. Die Referenzeinträge in der MAPI-Dokumentation enthalten einige Werte, die für jede Methode zurückgegeben werden können. Dies sind die Werte, die Ihr Client oder Dienstanbieter überprüfen und behandeln kann, da sie besondere Bedeutungen haben. Andere Werte können zurückgegeben werden, aber da sie nicht aussagekräftig sind, ist spezieller Code zur Behandlung dieser Werte nicht erforderlich. Eine einfache Überprüfung auf Erfolg oder Fehler ist ausreichend.
  
Einige der Schnittstellenmethoden geben Warnungen zurück. Wenn eine Methode, die Ihr Client oder Dienstanbieter aufruft, eine Warnung zurückgeben kann, verwenden Sie das **Makro HR_FAILED,** um den Rückgabewert zu testen, anstatt auf Null oder Null zu prüfen. Warnungen unterscheiden sich, auch wenn sie ungleich Null sind, von Fehlercodes darin, dass sie nicht über den High-Bit-Satz verfügen. Wenn Ihr Client oder Dienstanbieter das Makro nicht verwendet, ist es wahrscheinlich, dass bei einem Fehler eine Warnung angezeigt wird. 
  
Obwohl die meisten Schnittstellenmethoden und -funktionen HRESULT-Werte zurückgeben, geben einige Funktionen nicht signierte lange Werte zurück. Außerdem stammen einige in der MAPI-Umgebung verwendete Methoden von COM und geben COM-Fehlerwerte anstelle von MAPI-Fehlerwerten zurück. Beachten Sie beim Tätigen von Anrufen die folgenden Richtlinien:
  
- Verwenden Sie niemals die Rückgabewerte von **IUnknown::AddRef** oder **IUnknown::Release.** Diese Rückgabewerte dienen nur zu Diagnosezwecken. 
    
- **IUnknown::QueryInterface** gibt anstelle von MAPI-Fehlern immer generische COM-Fehler zurück, bei denen die Einrichtung FACILITY_NULL oder FACILITY_RPC ist. 
    
- Alle anderen Schnittstellenmethoden geben MAPI-Schnittstellenfehler mit einer Möglichkeit von FACILITY_ITF oder FACILITY_RPC oder FACILITY_NULL Zurück.
    
Wenn eine nicht unterstützte MAPI-Methode aufgerufen wird, kann einer von vier möglichen Fehlern zurückgegeben werden: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

