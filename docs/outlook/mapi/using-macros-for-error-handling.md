---
title: Verwenden von Makros zur Fehlerbehandlung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 351405ca-b72b-4e9e-bc8e-947344588970
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 715cd001c5eab89f40c31200a12deaf6981b9a61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567125"
---
# <a name="using-macros-for-error-handling"></a>Verwenden von Makros zur Fehlerbehandlung

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
   

