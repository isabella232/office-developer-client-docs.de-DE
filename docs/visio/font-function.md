---
title: FONT Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Gibt den Integer-Wert, der den eindeutigen Bezeichner für eine Schriftart, die durch Name angegebene zurück.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797050"
---
# <a name="font-function"></a>FONT Function

Gibt den Integer-Wert, der den eindeutigen Bezeichner für eine Schriftart, die durch Name angegebene zurück.
  
> [!NOTE]
> In den meisten Fällen wird die Schriftart-ID systemspezifische. Obwohl die Schriftart eingerichteten einmal in einer Datei verwendet bleibt, stellt die **Schriftart** Funktion konsistenten Zugriff auf eine bestimmte Schriftart System-und Versionen von Visio an. Es wird empfohlen, für die Verwendung der Funktion **Schriftart** Schriftarten anstatt direkt in Bezug auf die Schriftart Bezeichner zuweisen. 
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **Schriftart** ( _"Font_name_string"_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Erforderlich  <br/> |**string** <br/> |Der Name der Schriftart.  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

Ganze Zahl
  
## <a name="remarks"></a>Bemerkungen

Wenn die Zeichenfolge *Font_name_string* vorgesehenen nicht über eine bekannte Schriftart übereinstimmt, gibt diese Funktion ein #VALUE! Fehler. 
  
## <a name="example"></a>Beispiel

 `FONT("Calibri")`
  
Gibt den ganzzahligen Wert (4), die eindeutige ID für die Schriftart "Calibri" darstellt.
  

