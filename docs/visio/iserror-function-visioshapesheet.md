---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Gibt TRUE zurück, wenn der Wert von Zellbezug beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben. ISERROR-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797243"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR Function (VisioShapeSheet)

Gibt TRUE zurück, wenn der Wert von _Zellbezug_ beliebiger Fehlertyp ist. Andernfalls wird FALSE zurückgegeben. ISERROR-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERROR (** *Zellbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zellbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/V!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.a1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #N/V! erkennt. Mit der ISERROR-Funktion können Sie alle Fehlertypen außer dem Fehlertyp #N/V! verwenden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Haus"  <br/> |#WERT!  <br/> |
|Scratch.B1  <br/> |=IsError(Scratch.x1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #WERT! erkennt. Wenn Sie einen Ausdruck auf Basis des Fehlertyps #WERT! aufbauen möchten, verwenden Sie die Funktion ISERRVALUE.
  

