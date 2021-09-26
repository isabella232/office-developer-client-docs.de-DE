---
title: ISERROR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
ms.localizationpriority: medium
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Gibt TRUE zurück, wenn der Wert der CellReference einen Fehlertyp aufweist; andernfalls wird FALSE zurückgegeben. Die ISERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.
ms.openlocfilehash: b685f4fdc23e0935ddbf59b2082ad70db86ea9a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618791"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR-Funktion (VisioShapeSheet)

Gibt TRUE zurück, wenn der Wert der  _CellReference_ einen Fehlertyp aufweist; andernfalls wird FALSE zurückgegeben. Die ISERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERROR(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.A1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #N/V! erkennt. Mit der ISERROR-Funktion können Sie alle Fehlertypen außer dem Fehlertyp #N/V! verwenden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="House"  <br/> |#VALUE!  <br/> |
|Scratch.B1  <br/> |=ISERROR(Scratch.X1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #WERT! erkennt. Wenn Sie einen Ausdruck auf Basis des Fehlertyps #WERT! aufbauen möchten, verwenden Sie die Funktion ISERRVALUE.
  

