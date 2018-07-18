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
description: 'Gibt TRUE zurück, wenn der Wert von Zellbezug den Fehlertyp #n ist! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. ISERRNA-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797241"
---
# <a name="iserrna-function"></a>ISERRNA-Funktion

Gibt TRUE zurück, wenn der Wert von _Zellbezug_ den Fehlertyp #n ist! (nicht verfügbar); Andernfalls wird FALSE zurückgegeben. ISERRNA-Funktion wird in Formeln verwendet, die auf einer anderen Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERRNA (** *Zellbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zellbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |="5 + 3"  <br/> |"8"  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |FALSE  <br/> |
   
Gibt FALSE zurück, da der zurückgegebene Wert verfügbar ist.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/V!  <br/> |
|Scratch.B1  <br/> |=ISERRNA(Scratch.a1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da der Rückgabewert den Fehlertyp #N/V! ergibt.
  

