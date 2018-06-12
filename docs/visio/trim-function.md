---
title: TRIM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
localization_priority: Normal
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern.
ms.openlocfilehash: b396572041e880451ceb1ec6f0508528c0807bfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798319"
---
# <a name="trim-function"></a>TRIM Function

Entfernt alle Leerzeichen aus Text, mit Ausnahme einzelner Leerzeichen zwischen Wörtern. 
  
## <a name="syntax"></a>Syntax

TRIM (** *Text* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, aus dem die Leerzeichen entfernt werden sollen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Sie können die Funktion TRIM bei Texten verwenden, die aus einer anderen Anwendung übernommen wurden und überzählige Leerzeichen aufweisen.
  
## <a name="example"></a>Beispiel

TRIM ("Januar 1, 2003") 
  
Gibt "January 1, 2003" zurück. 
  

