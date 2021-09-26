---
title: ISERRNA-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
ms.localizationpriority: medium
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Gibt TRUE zurück, wenn der Wert der Zellreferenz den Fehlertyp #N/A! (nicht verfügbar); andernfalls wird FALSE zurückgegeben. Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: ad39cc4fb96600f90ff24673e591fbc409ae4d77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612596"
---
# <a name="iserrna-function"></a>ISERRNA-Funktion

Gibt TRUE zurück, wenn der Wert der  _Zellreferenz_ den Fehlertyp #N/A! (nicht verfügbar); andernfalls wird FALSE zurückgegeben. Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRNA(** *cellreference* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |FALSE  <br/> |
   
Gibt FALSE zurück, da der zurückgegebene Wert verfügbar ist.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formel**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.A1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da der Rückgabewert den Fehlertyp #N/V! ergibt.
  

