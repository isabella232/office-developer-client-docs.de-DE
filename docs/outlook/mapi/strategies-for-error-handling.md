---
title: Strategien zur Fehlerbehandlung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: be941efd-04b3-48d0-9b9c-8195ad2bb58d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e778df216d0fe9b901cd9f7136c8014a6b8f0d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795637"
---
# <a name="strategies-for-error-handling"></a>Strategien zur Fehlerbehandlung

  
  
**Betrifft**: Outlook 
  
Da Schnittstellenmethoden virtuellen sind, ist es nicht möglich, als ein Anrufer den vollständigen Satz von Werten kennen, die von jeder einen Aufruf zurückgegeben werden können. Eine Implementierung einer Methode möglicherweise fünf Werte zurück. eine andere möglicherweise acht zurück. Die Einträge Verweis in der Dokumentation zu MAPI-einige Werte aufgeführt, die für jede Methode zurückgegeben werden können; Dies sind die Werte, die der Client oder Dienstanbieter suchen und verarbeiten, da sie eine besondere Bedeutung haben kann. Andere Werte zurückgegeben werden können, aber, da sie nicht aussagekräftig sind, ist die Behandlung von spezieller Code nicht erforderlich. Eine einfache Überprüfung Erfolg oder Fehler ist ausreichend.
  
Wenige-Schnittstellenmethoden zurückgeben Warnungen. Wenn eine Methode, die der Client oder Dienstanbieter Ruft eine Warnung zurückgeben kann, verwenden Sie das Makro **HR_FAILED** So testen Sie den Rückgabewert statt eine Überprüfung für 0 (null) oder ungleich NULL. Warnungen, unterscheiden sich zwar ungleich NULL, von Fehlercodes, dass sie nicht das hohe Bit festgelegt haben. Wenn der Client oder Dienstanbieter nicht das Makro verwendet wird, ist es wahrscheinlich, dass eine Warnung für ein Fehler gehalten werden kann. 
  
Zwar die meisten Interface-Methoden und Funktionen HRESULT-Werte zurückgeben, Rückgabewerte einige Funktionen, die nicht signierte lang. Darüber hinaus einige Methoden in der MAPI-Umgebung verwendet stammen aus COM und COM-Fehlerwerte statt MAPI-Fehlerwerte zurückzugeben. Beachten behalten Sie die folgenden Richtlinien beim erachtet bei:
  
- Niemals, oder verwenden Sie die Rückgabewerte von **IUnknown:: AddRef** oder **IUnknown**. Diese zurückgegebenen Werte sind nur zu Diagnosezwecken. 
    
- **QueryInterface** gibt immer generischen COM-Fehler, in dem die Funktion FACILITY_NULL oder FACILITY_RPC wird, statt der MAPI-Fehler zurück. 
    
- Alle anderen Schnittstellenmethoden zurückgeben MAPI-Benutzeroberflächenfehler mit einer Funktion des FACILITY_ITF oder FACILITY_RPC oder FACILITY_NULL Fehler.
    
Wenn eine nicht unterstützte MAPI-Methode aufgerufen wird, kann eine der vier mögliche Fehler zurückgegeben werden: 
  
MAPI_E_NO_SUPPORT
  
MAPI_E_INTERFACE_NOT_SUPPORTED
  
MAPI_E_INVALID_PARAMETER
  
MAPI_E_VERSION. 
  

