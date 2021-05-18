---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422173"
---
# <a name="font-function"></a>FONT Function

Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine Schriftart zurück, der durch den Namen angegeben wird.
  
> [!NOTE]
> In den meisten Fällen ist der Schriftartenbezeichner systemspezifisch. Obwohl die Schriftart nach der Verwendung in einer Datei eingerichtet bleibt, bietet die **FONT-Funktion** einen konsistenten Zugriff auf eine bestimmte Schriftart über Systeme und Versionen von Visio. Es wird empfohlen, die **FONT-Funktion** zu verwenden, um Schriftarten zuzuordnen, anstatt direkt auf Schriftartbezeichner zu verweisen. 
  
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

Wenn die für die  *Font_name_string*  bereitgestellte Zeichenfolge nicht mit einer bekannten Schriftart übereinstimmen, gibt diese Funktion eine #VALUE! zurück. 
  
## <a name="example"></a>Beispiel

 `FONT("Calibri")`
  
Gibt den ganzzahligen Wert (4) zurück, der die eindeutige ID für die Schriftart "Calibri" darstellt.
  

