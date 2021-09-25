---
title: GETVAL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
ms.localizationpriority: medium
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn sich der Wert der Zelle ändert.
ms.openlocfilehash: fe5af032eae84612963913a23f94e65708e5ec8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582666"
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
  

