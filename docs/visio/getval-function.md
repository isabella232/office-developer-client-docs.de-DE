---
title: GETVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416888"
---
# <a name="getval-function"></a>GETVAL Function

Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.
  
## <a name="syntax"></a>Syntax

GETVAL(** *cellname* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Zelle, deren Wert abgerufen werden soll.  <br/> |
   
## <a name="example"></a>Beispiel

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Gibt den summierten Wert der Zellen PinX, PinY und Width zurück. 
  

