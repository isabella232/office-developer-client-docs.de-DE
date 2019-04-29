---
title: USERUI-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Wertet einen der beiden Ausdrücke in Abhängigkeit vom Wert von State aus.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420346"
---
# <a name="userui-function"></a>USERUI Function

Wertet einen der beiden Ausdrücke in Abhängigkeit vom Wert von _State_aus.
  
## <a name="syntax"></a>Syntax

USERUI (* * *Status* * *, * * *Standardwert* * *, * * *Benutzertyp* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, welcher Ausdruck ausgewertet werden soll.  <br/> |
| _DEFAULTAusdruck_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Standardausdruck.  <br/> |
| _UserForm_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein vom Benutzer bereitgestellter Ausdruck.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn _Status_ 0 ist, wertet die USERUI-Funktion den _Standard_Ausdruck aus. Wenn _Status_ 1 ist, wird die _Benutzer_Ausdruck ausgewertet.
  
## <a name="example"></a>Beispiel

USERUI (1, if (Breite\>6in, 6in, Breite), Breite\*0,75) 
  
Wertet den Ausdruck\*Width. 075 und gibt das Ergebnis zurück. 
  

