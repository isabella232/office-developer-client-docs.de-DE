---
title: ISERROR-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Gibt TRUE zurück, wenn der Wert von cellreference ein beliebiger Fehlertyp ist; Andernfalls wird FALSE zurückgegeben. Die isERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317892"
---
# <a name="iserror-function-visioshapesheet"></a>ISERROR-Funktion (VisioShapeSheet)

Gibt TRUE zurück, wenn der Wert von _cellreference_ ein beliebiger Fehlertyp ist; Andernfalls wird FALSE zurückgegeben. Die isERROR-Funktion wird in Formeln verwendet, die auf eine andere Zelle verweisen. 
  
## <a name="syntax"></a>Syntax

IsERROR (* * *cellreference* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellreference_ <br/> |Erforderlich  <br/> |**String** <br/> |Bezug auf eine Zelle.  <br/> |
   
## <a name="example-1"></a>Beispiel 1

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. a1  <br/> |=NV( )  <br/> |#N/A!  <br/> |
|Scratch. B1  <br/> |= IsERROR (Scratch. a1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #N/V! erkennt. Mit der ISERROR-Funktion können Sie alle Fehlertypen außer dem Fehlertyp #N/V! verwenden.
  
## <a name="example-2"></a>Beispiel 2

|**Cell**|**Formula**|**Zurückgegebener Wert**|
|:-----|:-----|:-----|
|Scratch. x1  <br/> |= "Haus"  <br/> |#VALUE!  <br/> |
|Scratch. B1  <br/> |= IsERROR (Scratch. x1)  <br/> |TRUE  <br/> |
   
Gibt TRUE zurück, da die ISERROR-Funktion den Fehler #WERT! erkennt. Wenn Sie einen Ausdruck auf Basis des Fehlertyps #WERT! aufbauen möchten, verwenden Sie die Funktion ISERRVALUE.
  

