---
title: MAGNITUDE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Gibt das Ausmaß der Vektor, dessen Steigung, deren Ausführung B, multipliziert mit den jeweiligen ist KonstanteA und KonstanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797435"
---
# <a name="magnitude-function"></a>MAGNITUDE Function

_Gibt dem Ausmaß der Vektor, dessen Steigung, deren Ausführung _B_, multipliziert mit der entsprechenden Konstanten ist_ _KonstanteA_ und _KonstanteB_. 
  
## <a name="syntax"></a>Syntax

MAGNITUDE (** *KonstanteA* **, ** *A* **, ** *KonstanteB* **, ** *B* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _KonstanteA_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Konstante, mit der die Steigung multipliziert werden soll.  <br/> |
| _A_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Steigung.  <br/> |
| _KonstanteB_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Konstante, mit der die Länge multipliziert werden soll.  <br/> |
| _B_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Länge.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

MAGNITUDE wird nach folgender Formel berechnet:
  
Wurzel ((KonstanteA \* A) ^ 2 + (KonstanteB \* B) ^ 2)
  
## <a name="example"></a>Beispiel

MAGNITUDE(1, 3, 1, 4) 
  
Gibt 5 zurück. 
  

