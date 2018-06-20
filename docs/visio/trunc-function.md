---
title: TRUNC-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Gibt eine Zahl auf die angegebene Anzahl von Ziffern gekürzt.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798311"
---
# <a name="trunc-function"></a>TRUNC Function

Gibt eine Zahl auf die angegebene Anzahl von Ziffern gekürzt.
  
## <a name="syntax"></a>Syntax

TRUNC (** *Anzahl* **, ** *AnzahlVonStellen* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Anzahl_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die zu kürzende Zahl.  <br/> |
| _AnzahlVonStellen_ <br/> |Erforderlich  <br/> |**Numerische** <br/> |Die Anzahl der Ziffern an die zu kürzende _Zahl_.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Numeric.
  
## <a name="remarks"></a>Bemerkungen

Wenn _AnzahlVonStellen_ größer als 0 ist, wird _Zahl_ auf die rechts vom Dezimalkomma _AnzahlVonStellen_ gekürzt. Wenn _AnzahlVonStellen_ 0 ist, wird _Zahl_ auf eine ganze Zahl gekürzt. Wenn _AnzahlVonStellen_ kleiner als 0 ist, wird _Zahl_ auf die links vom Dezimalkomma _AnzahlVonStellen_ gekürzt. 
  
## <a name="example-1"></a>Beispiel 1

TRUNC(123.654,2)
  
Gibt 123,65 zurück.
  
## <a name="example-2"></a>Beispiel 2

TRUNC(123.654,0)
  
Gibt 123 zurück.
  
## <a name="example-3"></a>Beispiel 3

TRUNC(123.654,-1)
  
Gibt 120 zurück.
  

