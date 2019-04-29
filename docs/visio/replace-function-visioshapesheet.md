---
title: REPLACE-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414354"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE-Funktion (VisioShapeSheet)

Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.
  
## <a name="syntax"></a>Syntax

REPLACE (* * *old_text* * *, * * *start_num* * *, * * *num_chars* * *, * * *new_text* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _old_text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, in dem einige Zeichen ersetzt werden sollen.  <br/> |
| _start_num_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Position des Zeichens in _old_text_ , das Sie durch _new_text_ersetzen möchten. Das erste Zeichen in der Zeichenfolge ist Position 1.  <br/> |
| _num_chars_ <br/> |Erforderlich  <br/> |**Number** <br/> |Die Anzahl der Zeichen in _old_text_ , die Sie ersetzen möchten.  <br/> |
| _new_text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, der Zeichen in _old_text_ersetzen wird.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktion REPLACE, wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in der Zeichenfolge auftritt. Wenn Sie bestimmten Text in einer Zeichenkette ersetzen möchten, verwenden Sie die Funktion SUBSTITUTE.
  
## <a name="example"></a>Beispiel

REPLACE ("01/03/2002",9,2,"03") 
  
Gibt 01/03/2003 zurück. 
  

