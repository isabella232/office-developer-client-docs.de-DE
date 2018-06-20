---
title: HASCATEGORY-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed3c997b-0a58-0432-c468-a24614b67f2e
description: Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
ms.openlocfilehash: 2445b4c3af63b331b303897997ce38b0747f17fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797142"
---
# <a name="hascategory-function"></a>HASCATEGORY-Funktion

Gibt TRUE zurück, wenn es sich die angegebene Zeichenfolge in der Kategorienliste des Shapes befindet.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2010 
  
## <a name="syntax"></a>Syntax

HASCATEGORY (** *Kategorie* **) 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _category_ <br/> |Erforderlich  <br/> |**String** <br/> |Die zu suchende Kategorie.  <br/> |
   
### <a name="return-value"></a>Rückgabewert

 **Boolean**
  
## <a name="remarks"></a>Hinweise

 *Kategorien* sind benutzerdefinierte Zeichenfolgen, die Sie verwenden können, die Shapes kategorisieren. Sie können die Kategorien in der Zelle User.msvShapeCategories im ShapeSheet für ein Shape definieren. Sie können mehrere Kategorien für ein Shape definieren, indem Sie die Kategorien durch ein Semikolon voneinander getrennt. 
  

