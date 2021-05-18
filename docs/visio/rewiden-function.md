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
description: Wandelt eine Formel, die 16-Bit-Zeichencodes erzeugt, die mit einem Byte oder einem Mehrbyte-Zeichensatz in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes mit den angegebenen Zeichensätzen verbreitet werden.
ms.openlocfilehash: c885487f91e541027b7ba09812e7321a9deb00ac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405212"
---
# <a name="rewiden-function"></a>REWIDEN Function

Wandelt eine Formel, die 16-Bit-Zeichencodes erzeugt, die mit einem Byte oder einem Mehrbyte-Zeichensatz in eine Zeichenfolge mit 16-Bit-Unicode-Zeichencodes mit den angegebenen Zeichensätzen verbreitet werden. 
  
## <a name="syntax"></a>Syntax

REWIDEN(** *srcCharSet* **, ** *dstCharSet* **, ** *text* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _srcCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> |Der Zeichensatz im Quelldokument.  <br/> |
| _dstCharSet_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Zeichensatz im Zieldokument.  <br/> |
| _text_ <br/> |Erforderlich  <br/> |**String** <br/> |Der zu konvertierende Text.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die REWIDEN-Funktion wird zur automatischen Konvertierung von Visio 2002-Dokumenten in Visio 2003-Dokumente verwendet. Eine andere Verwendung wird nicht empfohlen.
  

