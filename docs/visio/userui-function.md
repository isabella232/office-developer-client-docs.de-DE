---
title: USERUI-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
ms.localizationpriority: medium
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Wertet einen der beiden Ausdrücke in Abhängigkeit vom Statuswert aus.
ms.openlocfilehash: 8e26154b6d6f4f8102380d03ee95417a09994567
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549357"
---
# <a name="userui-function"></a>USERUI Function

Wertet einen der beiden Ausdrücke in Abhängigkeit vom  _Statuswert_ aus.
  
## <a name="syntax"></a>Syntax

USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, welcher Ausdruck ausgewertet werden soll.  <br/> |
| _defaultexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Standardausdruck.  <br/> |
| _userexpression_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein vom Benutzer bereitgestellter Ausdruck.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn  _der Status_ 0 ist, wertet die USERUI-Funktion den  _Defaultexpression_ aus. Wenn  _der Status_ 1 ist, wird der  _Userexpression_ ausgewertet.
  
## <a name="example"></a>Beispiel

USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0,75) 
  
Wertet den Ausdruck Width \* .075 aus und gibt das Ergebnis zurück. 
  

