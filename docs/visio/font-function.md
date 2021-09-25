---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.
ms.openlocfilehash: 9211d56299cbf3085de4060921b19b6a0ed414e6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574230"
---
# <a name="font-function"></a>FONT Function

Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.
  
> [!NOTE]
> In den meisten Fällen ist der Schriftbezeichner systemspezifisch. Obwohl die Schriftart nach der Verwendung in einer Datei weiterhin hergestellt wird, bietet die **FONT-Funktion** einen konsistenten Zugriff auf eine bestimmte Schriftart über Systeme und Versionen von Visio hinweg. Es wird empfohlen, schriftarten mithilfe der **FONT-Funktion** zuzuweisen, anstatt direkt auf Schriftartbezeichner zu verweisen. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **FONT**( _"font_name_string"_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Erforderlich  <br/> |**Zeichenfolge** <br/> |Der Name der Schriftart.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn die für  *font_name_string*  angegebene Zeichenfolge nicht mit einer bekannten Schriftart übereinstimmt, gibt diese Funktion eine #VALUE! zurück. 
  
## <a name="example"></a>Beispiel

 `FONT("Calibri")`
  
Gibt den ganzzahligen Wert (4) zurück, der die eindeutige ID für die Schriftart "Calibri" darstellt.
  

