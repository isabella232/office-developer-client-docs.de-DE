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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327314"
---
# <a name="getval-function"></a>GETVAL Function

Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.
  
## <a name="syntax"></a>Syntax

GETVAL (* * *cellName* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Zelle, deren Wert abgerufen werden soll.  <br/> |
   
## <a name="example"></a>Beispiel

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Gibt den summierten Wert der Zellen PinX, PinY und Width zurück. 
  

