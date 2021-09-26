---
title: ISERR-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
ms.localizationpriority: medium
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Gibt TRUE zurück, wenn der Wert der Zellreferenz einen Fehlertyp mit Ausnahme von #N/A aufweist; andernfalls wird FALSE zurückgegeben. Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: bb724fdb753ada86baf6cb421a2fa758620317ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612610"
---
# <a name="iserr-function"></a>ISERR Function

Gibt TRUE zurück, wenn der Wert der  _CellReference_ einen Fehlertyp mit Ausnahme von #N/A aufweist; andernfalls wird FALSE zurückgegeben. Die ISERR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.A1)  <br/> |FALSE  <br/> |
   
Gibt FALSE zurück, da die ISERR-Funktion den Fehler #N/V! nicht erkennt. Verwenden Sie ISERROR, um alle Fehlertypen zu finden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die Funktion ISERR den Fehler #WERT! erkennt.
  

