---
title: REWIDEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
localization_priority: Normal
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Konvertiert eine Formel, die 16-Bit-Zeichencodes, die erweiterte Einzel-Byte oder multibyte-Zeichensatz Codes in eine Zeichenfolge von 16-Bit-Unicode-Zeichencodes erzeugt, mithilfe der angegebenen Zeichensätze aufweisen.
ms.openlocfilehash: 66dc3e801585077a9521cd93f8ae78c47f8a746b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797862"
---
# <a name="rewiden-function"></a>REWIDEN Function

Konvertiert eine Formel, die 16-Bit-Zeichencodes, die erweiterte Einzel-Byte oder multibyte-Zeichensatz Codes in eine Zeichenfolge von 16-Bit-Unicode-Zeichencodes erzeugt, mithilfe der angegebenen Zeichensätze aufweisen. 
  
## <a name="syntax"></a>Syntax

REWIDEN (** *SrcCharSet* **, ** *DstCharSet* **, ** *Text* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Zeichensatz im Quelldokument.  <br/> |
| _dstCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Zeichensatz im Zieldokument.  <br/> |
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der zu konvertierende Text.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.
  

