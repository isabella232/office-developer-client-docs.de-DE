---
title: POW-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Gibt eine Zahl zurück, die auf die Macht eines Exponenten angehoben wird.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406311"
---
# <a name="pow-function"></a>POW Function

Gibt eine Zahl zurück, die auf die Macht eines Exponenten angehoben wird.
  
## <a name="syntax"></a>Syntax

POW(** *Number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Zahl, die mit einem Exponenten potenziert werden soll.  <br/> |
| _exponent_ <br/> |Erforderlich  <br/> |**Number** <br/> |Der Exponent.  <br/> |
   
## <a name="remarks"></a>Hinweise

Sowohl  _Zahl_ als  _auch Exponent_ können nicht ganzzahlig sein, und sie können negativ sein. Wenn  _Zahl_ nicht 0 und  _Exponent_ 0 ist, gibt diese Funktion 1 zurück. Wenn  _Zahl_ 0 und  _Exponent_ negativ ist, gibt diese Funktion 0,0 zurück. Wenn Zahl _und_ _Exponent_ 0  sind oder Zahl negativ ist und _exponent_ keine ganze Zahl ist, gibt diese Funktion 0,0 zurück. Wenn Zahl  _und_  _Exponent_ negativ sind, gibt diese Funktion -1,#IND. 
  
## <a name="example"></a>Beispiel

POW(5,2) 
  
Gibt 25 zurück. 
  

