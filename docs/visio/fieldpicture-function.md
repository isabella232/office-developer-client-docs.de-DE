---
title: FIELDPICTURE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251592
localization_priority: Normal
ms.assetid: df88c55f-c098-dd4c-bf53-c7d7b60cf719
description: Gibt eine Zeichenfolge zum Formatieren von Bildern zurück, die dem internen Textfeld-Formatcode von Microsoft Visio entspricht.
ms.openlocfilehash: 1ab24c602c7975cf6be22a564a8b9ee9aa0d6f46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431456"
---
# <a name="fieldpicture-function"></a>FIELDPICTURE Function

Gibt eine Zeichenfolge zum Formatieren von Bildern zurück, die dem internen Textfeld-Formatcode von Microsoft Visio entspricht.
  
## <a name="syntax"></a>Syntax

FIELDPICTURE(** *code* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _code_ <br/> |Erforderlich  <br/> |**Number** <br/> | Ein Textfeld-Formatcode.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Hinweise

Zeichenfolgen für Formatierungsangaben werden in der FORMAT-Funktion verwendet, um die Expandierung von Werten zu Datumsangaben, Zeitangaben, Zahlen und Einheitenbeschriftungen zu definieren.
  
## <a name="example"></a>Beispiel

FIELDPICTURE(0) 
  
Gibt die Zeichenfolge für eine Formatierungsangabe "0,0" zurück, die eine Zahl mit einer Dezimalstelle und eine Einheitenbeschreibung in Kleinbuchstaben festlegt, wenn sie in der FORMAT-Funktion verwendet wird. 
  

