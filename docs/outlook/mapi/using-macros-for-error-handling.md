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
ms.openlocfilehash: c4e216f2204f4ee97d9eeac81f77ce6a82fff3f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795822"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros zur Fehlerbehandlung

  
  
**Betrifft**: Outlook 
  
Es gibt mehrere Makros für entwickelt HRESULT-Werte zu erleichtern.
  
Es gibt zwei Sätze von Makros, die für Fehler oder Erfolg zu testen: HR_SUCCEEDED und HR_FAILED und SUCCEEDED und FAILED. Erfolgreich abgeschlossen wurde, handelt es sich um dieselbe wie HR_SUCCEEDED und fehlgeschlagen HR_FAILED identisch ist.
  
In diesem Fall verwenden Sie das Makro **ResultFromScode** , um die HRESULT-Variable auf den entsprechenden HRESULT-Wert für S_OK festzulegen. 
  
Häufig verwendete Makros werden in der folgenden Tabelle kurz beschrieben.
  
|**Makro**|**Beschreibung**|
|:-----|:-----|
|**MAKE_HRESULT** <br/> |Erstellt ein HRESULT aus seiner Komponenten.  <br/> |
|**HR_SUCCEEDED** <br/> |Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.  <br/> |
|**HR_FAILED** <br/> |Ein HRESULT für ein Fehlerzustand getestet.  <br/> |
|**HRESULT_CODE** <br/> |Den Fehler Codeteil der HRESULT extrahiert.  <br/> |
|**HRESULT_FACILITY** <br/> |Extrahiert die Einrichtung von HRESULT.  <br/> |
|**HRESULT_SEVERITY** <br/> |Extrahiert das Severity Bit Schweregrad.  <br/> |
|**ERFOLGREICH ABGESCHLOSSEN WURDE** <br/> |Ein HRESULT für einen Erfolg oder eine Warnung Bedingung getestet.  <br/> |
|**FEHLER BEI** <br/> |Ein HRESULT für ein Fehlerzustand getestet.  <br/> |
   

