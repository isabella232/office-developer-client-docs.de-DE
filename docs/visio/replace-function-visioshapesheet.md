---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797815"
---
# <a name="replace-function-visioshapesheet"></a>REPLACE Function (VisioShapeSheet)

Ersetzt auf der Grundlage der angegebenen Anzahl von Zeichen einen Teil einer Zeichenfolge durch eine andere Zeichenfolge.
  
## <a name="syntax"></a>Syntax

Ersetzen Sie (** *Alter_Text* **, ** *Erstes_Zeichen* **, ** *Num_chars* **, ** *Neuer_Text* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Alter_Text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, in dem einige Zeichen ersetzt werden sollen.  <br/> |
| _Erstes_Zeichen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Position des Zeichens in _Alter_Text_ , den Sie durch _Neuer_Text_ersetzen möchten. Das erste Zeichen in der Zeichenfolge ist Position 1.  <br/> |
| _Anzahl_Zeichen_ <br/> |Erforderlich  <br/> |**Nummer** <br/> |Die Anzahl der Zeichen in _Old_text_ , die Sie ersetzen möchten.  <br/> |
| _Neuer_Text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Text, der Zeichen in _Old_text_ersetzt werden sollen.  <br/> |
   
### <a name="return-value"></a>R�ckgabewert

Zeichenfolge
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie die Funktion REPLACE, wenn Sie Text ersetzen möchten, der an einer bestimmten Stelle in der Zeichenfolge auftritt. Wenn Sie bestimmten Text in einer Zeichenkette ersetzen möchten, verwenden Sie die Funktion SUBSTITUTE.
  
## <a name="example"></a>Beispiel

REPLACE ("01/03/2002",9,2,"03") 
  
Gibt 01/03/2003 zurück. 
  

