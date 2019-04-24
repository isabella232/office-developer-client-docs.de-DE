---
title: Verwenden von Makros zur Fehlerbehandlung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9e6901d6583e7a7924a4a7c19c0a262bcef74bd3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329659"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros zur Fehlerbehandlung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt mehrere Makros, um die Arbeit mit HRESULT-Werten zu vereinfachen.
  
Es gibt zwei Gruppen von Makros, die auf Fehler oder Erfolg testen: HR_SUCCEEDED und HR_FAILED und erfolgreich und fehlgeschlagen. SUCCEEDed ist identisch mit HR_SUCCEEDED und FAILED ist identisch mit HR_FAILED.
  
Verwenden Sie in diesem Fall das **ResultFromScode** -Makro, um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen. 
  
Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.
  
|**Makro**|**Beschreibung**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Erstellt ein HRESULT aus seinen Komponenten.  <br/> |
|**HR_SUCCEEDED** <br/> |Testet ein HRESULT für eine Erfolgs-oder Warnungsbedingung.  <br/> |
|**HR_FAILED** <br/> |Testet ein HRESULT auf eine Fehlerbedingung.  <br/> |
|**HRESULT_CODE** <br/> |Extrahiert den Fehlercode Teil von HRESULT.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrahiert die Einrichtung aus dem HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrahiert das Schweregrad-Bit aus dem Schweregrad.  <br/> |
|**GELUNGEN** <br/> |Testet ein HRESULT für eine Erfolgs-oder Warnungsbedingung.  <br/> |
|**NICHT** <br/> |Testet ein HRESULT auf eine Fehlerbedingung.  <br/> |
   

