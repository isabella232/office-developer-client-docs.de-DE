---
title: Verwenden von Makros für die Fehlerbehandlung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0d3c10a167c961dd2dfe8e31313f6b0f5d827abe
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619498"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros für die Fehlerbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt mehrere Makros, um die Arbeit mit HRESULT-Werten zu vereinfachen.
  
Es gibt zwei Makrogruppen, die auf Fehler oder Erfolg testen: HR_SUCCEEDED und HR_FAILED sowie SUCCEEDED und FAILED. SUCCEEDED ist identisch mit HR_SUCCEEDED und FAILED ist identisch mit HR_FAILED.
  
Verwenden Sie in diesem Fall das **Makro ResultFromScode,** um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen. 
  
Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.
  
|**Makro**|**Beschreibung**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Erstellt ein HRESULT aus seinen Komponenten.  <br/> |
|**HR_SUCCEEDED** <br/> |Testet ein HRESULT auf eine Erfolgs- oder Warnbedingung.  <br/> |
|**HR_FAILED** <br/> |Testet ein HRESULT auf eine Fehlerbedingung.  <br/> |
|**HRESULT_CODE** <br/> |Extrahiert den Fehlercodeteil des HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrahiert die Einrichtung aus dem HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrahiert das Schweregradbit aus dem SCHWEREGRAD.  <br/> |
|**GELUNGEN** <br/> |Testet ein HRESULT auf eine Erfolgs- oder Warnbedingung.  <br/> |
|**FEHLGESCHLAGEN** <br/> |Testet ein HRESULT auf eine Fehlerbedingung.  <br/> |
   

