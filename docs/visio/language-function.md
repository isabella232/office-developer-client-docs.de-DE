---
title: LANGUAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Ermöglicht Vergleichsvorgänge zwischen verschiedenen Sprachdarstellungen. Es wird am besten zum Konvertieren von BCP 47-Werten (Internet Engineering Task Force Language Tags) in Gebietsschema-ID-Werte (LCID) verwendet.
ms.openlocfilehash: 319d1a043b43f80accfe5b195a640acaea5a1c52
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554516"
---
# <a name="language-function"></a>LANGUAGE-Funktion

Ermöglicht Vergleichsvorgänge zwischen verschiedenen Sprachdarstellungen. Es wird am besten zum Konvertieren von BCP 47-Werten (Internet Engineering Task Force Language Tags) in Gebietsschema-ID-Werte (LCID) verwendet.
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **LANGUAGE**( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Erforderlich  <br/> |**String** <br/> |Der LCID- oder BCP 47-Wert für die Sprache.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="example"></a>Beispiel

 `LANGUAGE("en-us")`
  
Gibt den Wert "1033" zurück.
  
 `LANGUAGE("es-es")`
  
Gibt den Wert "3082" zurück.
  

