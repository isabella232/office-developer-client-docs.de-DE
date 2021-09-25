---
title: GETREF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
ms.localizationpriority: medium
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn sich die Zelle ändert, auf die verwiesen wird.
ms.openlocfilehash: b2331b18ed78583e745472b02736bd21fb45a104
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628290"
---
# <a name="getref-function"></a>GETREF Function

Verweist auf eine Zelle und berechnet die Formel nicht neu, wenn sich die Zelle ändert, auf die verwiesen wird.
  
## <a name="syntax"></a>Syntax

GETREF(** *cellname* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _cellname_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Name der Zelle, auf die ein Verweis abgerufen werden soll.  <br/> |
   
## <a name="example"></a>Beispiel

SETF(GETREF(PinX),5.1) 
  
Legt die Formel der Zelle DrehbezX auf 5,1 fest. 
  

