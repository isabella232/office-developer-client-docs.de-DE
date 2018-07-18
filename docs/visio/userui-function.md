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
description: Wertet einen der beiden Ausdrücke abhängig vom Wert des Status aus.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798369"
---
# <a name="userui-function"></a>USERUI Function

Wertet einen der beiden Ausdrücke abhängig vom Wert des _Status_aus.
  
## <a name="syntax"></a>Syntax

USERUI (** *Zustand* **, ** *Standardausdruck aus* **, ** *BenutzerAusdruck ausgewertet* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _state_ <br/> |Erforderlich  <br/> |**Boolean** <br/> |Bestimmt, welche der auszuwertende Ausdruck.  <br/> |
| _Standardausdruck aus_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Standardausdruck.  <br/> |
| _BenutzerAusdruck ausgewertet_ <br/> |Erforderlich  <br/> |**String** <br/> |Ein Ausdruck, der vom Benutzer bereitgestellt wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn _Zustand_ 0 ist, wertet die USERUI-Funktion den _Standardausdruck aus_. Wenn _Zustand_ 1 ist, wird der _BenutzerAusdruck ausgewertet_.
  
## <a name="example"></a>Beispiel

USERUI (1, wenn (Breite\>6 Zoll, 6 In, Breite), Breite\*0,75) 
  
Wertet den Ausdruck Breite\*.075 und gibt das Ergebnis zurück. 
  

