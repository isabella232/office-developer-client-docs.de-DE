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
description: Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn der Wert der Zelle ändert.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797095"
---
# <a name="getval-function"></a>GETVAL Function

Ruft den Wert einer Zelle ab und berechnet die Formel nicht neu, wenn der Wert der Zelle ändert.
  
## <a name="syntax"></a>Syntax

GETVAL (** *Abrufen Cellname* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _abrufen cellName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Zelle, deren Wert abgerufen werden soll.  <br/> |
   
## <a name="example"></a>Beispiel

GETVAL(PinX) + GETVAL(PinY) + Width 
  
Gibt den summierten Wert der Zellen PinX, PinY und Width zurück. 
  

