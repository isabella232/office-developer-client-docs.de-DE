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
description: 'Gibt true zurück, wenn der Wert von Zellbezug beliebiger Fehlertyp #n /; Andernfalls wird FALSE zurückgegeben. Die Funktion ISERR wird in Formeln verwendet, die auf einer anderen Zelle verweisen.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797229"
---
# <a name="iserr-function"></a>ISERR Function

Gibt True, wenn der Wert von _Zellbezug_ beliebiger Fehlertyp #n /; Andernfalls wird FALSE zurückgegeben. Die Funktion ISERR wird in Formeln verwendet, die auf einer anderen Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

ISERR (** *Zellbezug* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Zellbezug_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.A1  <br/> |=NV( )  <br/> |#N/V!  <br/> |
|Scratch.B1  <br/> |=ISERR(Scratch.a1)  <br/> |FALSCH  <br/> |
   
Gibt FALSE zurück, da die ISERR-Funktion den Fehler #N/V! nicht erkennt. Verwenden Sie ISERROR, um alle Fehlertypen zu finden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch.X1  <br/> |="Haus"  <br/> |#WERT!  <br/> |
|Scratch.A1  <br/> |=ISERR(Scratch.x1)  <br/> |WAHR  <br/> |
   
Gibt TRUE zurück, da die Funktion ISERR den Fehler #WERT! erkennt.
  

