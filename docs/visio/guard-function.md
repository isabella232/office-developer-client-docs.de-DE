---
title: GUARD-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Schützt Ausdruck vor dem Löschen und Ändern von Aktionen, die ausgeführt werden im Zeichnungsfenster, beispielsweise durch Verschieben, Verändern der Größe gruppieren oder Gruppierung der Shapes aufzuheben.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797116"
---
# <a name="guard-function"></a>GUARD Function

Schützt *Ausdruck* vor dem Löschen und Ändern von Aktionen, die ausgeführt werden im Zeichnungsfenster, beispielsweise durch Verschieben, Verändern der Größe gruppieren oder Gruppierung der Shapes aufzuheben. 
  
## <a name="syntax"></a>Syntax

GUARD (** *Ausdruck* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Erforderlich  <br/> |**String** <br/> |Eine Kombination aus Konstanten, Operatoren, Funktionen und Bezügen auf ShapeSheet-Zellen, die einen Wert ergeben.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Zu den Zellen, auf die sich die GUARD-Funktion am häufigsten auswirkt, zählen Breite, Höhe, DrehbezX und DrehbezY. 
  
Durch Schützen einer Zellformel verhindern Sie, dass der Wert dieser Zelle nicht durch im Zeichenfenster ausgeführte Aktionen verändert wird. Eine einzelne Aktion in dem Zeichenfenster kann sich jedoch auf mehrere Zellen auswirken. Jede dieser einzelnen Zellen muss geschützt werden, wenn Sie unerwartete Änderungen an der Darstellung eines Shapes verhindern möchten. 
  
## <a name="example"></a>Beispiel

GUARD(TEXTBREITE(DerText) + 0,5 in) 
  
Dieser Ausdruck in der Zelle Breite im Abschnitt Shape Transform eines Shapes verhindert, dass der Ausdruck (TEXTWIDTH(DerText) + 0,5 in) durch einen anderen Wert ersetzt wird, wenn die Breite des Shapes im Zeichnungsfenster geändert wird. Bei dem Text handelt es sich um eine Zelle, die bei Änderung der Textgestaltung des zugeordneten Shapes ausgelöst wird. 
  

