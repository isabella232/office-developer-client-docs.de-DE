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
description: Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn die referenzierte Zelle ändert.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797093"
---
# <a name="getref-function"></a>GETREF Function

Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn die referenzierte Zelle ändert.
  
## <a name="syntax"></a>Syntax

GETREF (** *Abrufen Cellname* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _abrufen cellName_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der abzurufenden einen Verweis auf die Zelle.  <br/> |
   
## <a name="example"></a>Beispiel

SETF(GETREF(PinX),5.1) 
  
Legt die Formel der Zelle DrehbezX auf 5,1 fest. 
  

