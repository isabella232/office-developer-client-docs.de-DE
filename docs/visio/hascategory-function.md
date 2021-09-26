---
title: HASCATEGORY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
ms.openlocfilehash: 953894bbc2914a363c4db99338528fa5f8ac7504
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598542"
---
# <a name="hascategory-function"></a>HASCATEGORY Function

Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

HASCATEGORY(** *category* ** ) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Kategorie_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu suchende Kategorie.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Boolean**
  
## <a name="remarks"></a>Bemerkungen

 *Kategorien*  sind benutzerdefinierte Zeichenfolgen, die Sie zum Kategorisieren von Shapes verwenden können. Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden. Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen. 
  

