---
title: HASCATEGORY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
ms.openlocfilehash: 902819f981b53aed96695e181ab556d3841d97c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360165"
---
# <a name="hascategory-function"></a>HASCATEGORY Function

Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010
 
  
## <a name="syntax"></a>Syntax

HASCATEGORY (* * *Category* * *) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _Kategorie_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu suchende Kategorie.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Boolean**
  
## <a name="remarks"></a>Hinweise

 *Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, um Shapes zu kategorisieren. Kategorien können in der Zelle User.msvShapeCategories im ShapeSheet eines Shapes definiert werden. Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch Semikolons trennen. 
  

