---
title: REWIDEN-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033808
ms.localizationpriority: medium
ms.assetid: c20842cd-86b1-83fa-49ba-118936013b6f
description: Konvertiert eine Formel, die 16-Bit-Zeichencodes erzeugt, die einbyte- oder mehrbyte-Zeichensatzcodes mithilfe der angegebenen Zeichensätze in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes erweitert werden.
ms.openlocfilehash: 35dc1f379c2fd0efc68f31ea92891d2b7914f3b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627632"
---
# <a name="rewiden-function"></a>REWIDEN Function

Konvertiert eine Formel, die 16-Bit-Zeichencodes erzeugt, die einbyte- oder mehrbyte-Zeichensatzcodes mithilfe der angegebenen Zeichensätze in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes erweitert werden. 
  
## <a name="syntax"></a>Syntax

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Zeichensatz im Quelldokument.  <br/> |
| _dstCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Zeichensatz im Zieldokument.  <br/> |
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der zu konvertierende Text.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.
  

