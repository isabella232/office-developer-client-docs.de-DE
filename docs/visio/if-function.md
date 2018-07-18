---
title: IF-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: Gibt WertWennWahr zurück, wenn Logicalexpression wahr ist. Andernfalls ihn Funktion Valueiffalse zurück.
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797187"
---
# <a name="if-function"></a>IF Function

Gibt _WertWennWahr_ zurück, wenn _Logicalexpression_ wahr ist. Andernfalls ihn _Funktion Valueiffalse zurück_.
  
## <a name="syntax"></a>Syntax

IF (** *Logicalexpression* **, ** *WertWennWahr* **, ** *Funktion Valueiffalse zurück* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _logicalexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der auszuwertende Ausdruck.  <br/> |
| _WertWennWahr_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Der zurückzugebende Wert, wenn _Logicalexpression_ wahr ist.  <br/> |
| _Funktion Valueiffalse zurück_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Der zurückzugebende Wert, wenn _Logicalexpression_ falsch ist.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Varies
  
## <a name="example"></a>Beispiel

IF (Höhe \> 1,25 in, 5, 7)
  
Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist. Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.
  

