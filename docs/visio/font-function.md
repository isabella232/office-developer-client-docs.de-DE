---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine durch Name angegebene Schriftart zurück.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346137"
---
# <a name="font-function"></a>FONT Function

Gibt den ganzzahligen Wert des eindeutigen Bezeichners für eine durch Name angegebene Schriftart zurück.
  
> [!NOTE]
> In den meisten Fällen ist die Schriftart-ID systemspezifisch. Obwohl die Schriftart nach der Verwendung in einer Datei festgelegt bleibt, bietet die **Font** -Funktion einen konsistenten Zugriff auf eine bestimmte Schriftart in Systemen und Versionen von Visio. Es wird empfohlen, dass Sie die **Font** -Funktion verwenden, um Schriftarten zuzuweisen, statt direkt auf Schriftart Bezeichner zu verweisen. 
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **Schriftart** ( _"font_name_string"_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Erforderlich  <br/> |**Zeichenfolge** <br/> |Der Name der Schriftart.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn die für *font_name_string* angegebene Zeichenfolge nicht mit einer bekannten Schriftart übereinstimmt, gibt diese funktion einen #VALUE! zurück. 
  
## <a name="example"></a>Beispiel

 `FONT("Calibri")`
  
Gibt den ganzzahligen Wert (4) zurück, der die eindeutige ID für die Schriftart "Calibri" darstellt.
  

