---
title: ISERRNA-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Gibt TRUE zurück, wenn der Wert von cellreference den Fehlertyp #N/A! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432114"
---
# <a name="iserrna-function"></a>ISERRNA-Funktion

Gibt TRUE zurück, wenn der Wert von _cellreference_ den fehlertyp #N/a! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. Die ISERRNA-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRNA (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |="5 + 3"  <br/> |8  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |FALSE  <br/> |
   
Gibt FALSE zurück, da der zurückgegebene Wert verfügbar ist.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= ISERRNA (Scratch. a1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da der Rückgabewert den Fehlertyp #N/V! ergibt.
  

