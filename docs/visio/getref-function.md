---
title: GETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn sich die referenzierte Zelle ändert.
ms.openlocfilehash: 38f3c8b4f34ed2b3d3711be5faed6b0d317e907a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424329"
---
# <a name="getref-function"></a>GETREF Function

Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn sich die referenzierte Zelle ändert.
  
## <a name="syntax"></a>Syntax

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Zelle, auf die verwiesen werden soll.  <br/> |
   
## <a name="example"></a>Beispiel

SETF(GETREF(PinX),5.1) 
  
Legt die Formel der Zelle DrehbezX auf 5,1 fest. 
  

