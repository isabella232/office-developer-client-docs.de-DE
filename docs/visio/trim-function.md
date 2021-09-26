---
title: TRIM-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027318
ms.localizationpriority: medium
ms.assetid: 6f2d84fd-27eb-4c2f-a2e1-43d20e0c78be
description: Entfernt den gesamten Textbereich mit Ausnahme einzelner Leerzeichen zwischen Wörtern.
ms.openlocfilehash: e6d8263585754db88a1500a5fbe20a56ef4fe633
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627261"
---
# <a name="trim-function"></a>TRIM Function

Entfernt den gesamten Textbereich mit Ausnahme einzelner Leerzeichen zwischen Wörtern. 
  
## <a name="syntax"></a>Syntax

TRIM (** *text* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, aus dem die Leerzeichen entfernt werden sollen.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Sie können die Funktion TRIM bei Texten verwenden, die aus einer anderen Anwendung übernommen wurden und überzählige Leerzeichen aufweisen.
  
## <a name="example"></a>Beispiel

TRIM ("1. Januar 2003") 
  
Gibt "January 1, 2003" zurück. 
  

