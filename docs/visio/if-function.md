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
description: Gibt Wahrheitsprüfung ungleich zurück, wenn logicive auf TRUE festgelegt ist. Andernfalls wird den sonst zurückgegeben.
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405471"
---
# <a name="if-function"></a>IF Function

Gibt _Wahrheitsprüfung ungleich_ zurück __ , wenn logicive auf true festgelegt ist. Andernfalls wird _den sonst_zurückgegeben.
  
## <a name="syntax"></a>Syntax

IF (* * *logischer* * *, * * *Wahrheitsprüfung ungleich* * *, * * *den sonst* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Logik_ <br/> |Erforderlich  <br/> |**String** <br/> |Der auszuwertende Ausdruck.  <br/> |
| _Wahrheitsprüfung ungleich_ <br/> |Erforderlich  <br/> |**Variiert** <br/> |Wert, der zurückgegeben werden soll, wenn die _Logik_ true ist.  <br/> |
| _den sonst_ <br/> |Erforderlich  <br/> |**Variiert** <br/> | Wert, der zurück __ gegeben werden soll, wenn logisches false ist.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Variiert
  
## <a name="example"></a>Beispiel

IF (Höhe \> 1,25 in, 5, 7)
  
Gibt 5 zurück, wenn die Höhe des Shapes größer als 3 cm ist. Gibt 7 zurück, wenn die Höhe des Shapes kleiner als oder gleich 3 cm ist.
  

