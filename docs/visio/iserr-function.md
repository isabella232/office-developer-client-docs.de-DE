---
title: ISERR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Gibt TRUE zurück, wenn der Wert von cellreference ein beliebiger Fehlertyp ist, außer #N/A; Andernfalls wird FALSE zurückgegeben. Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432107"
---
# <a name="iserr-function"></a>ISERR Function

Gibt TRUE zurück, wenn der Wert von _cellreference_ ein beliebiger Fehlertyp ist, außer #N/a; Andernfalls wird FALSE zurückgegeben. Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERR (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERR (Scratch. a1)  <br/> |FALSE  <br/> |
   
Gibt FALSE zurück, da die ISERR-Funktion den Fehler #N/V! nicht erkennt. Verwenden Sie ISERROR, um alle Fehlertypen zu finden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. x1  <br/> |= "Haus"  <br/> |#VALUE!  <br/> |
|Scratch. a1  <br/> |= ISERR (Scratch. x1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die Funktion ISERR den Fehler #WERT! erkennt.
  

