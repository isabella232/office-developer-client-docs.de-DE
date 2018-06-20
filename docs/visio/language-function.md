---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Der Vergleichsvorgänge zwischen anderen Sprache Darstellungen ermöglicht. Es ist am besten für die Konvertierung von Tags (BCP 47) Werte der Internet Engineering Task Force Language, Werte für den Gebietsschemabezeichner (LCID) verwendet.
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797298"
---
# <a name="language-function"></a>LANGUAGE Function

Der Vergleichsvorgänge zwischen anderen Sprache Darstellungen ermöglicht. Es ist am besten für die Konvertierung von Tags (BCP 47) Werte der Internet Engineering Task Force Language, Werte für den Gebietsschemabezeichner (LCID) verwendet.
  
## <a name="version-information"></a>Versionsinformationen

Hinzugefügte Version: Visio 2013 
  
## <a name="syntax"></a>Syntax

 **Sprache** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Erforderlich  <br/> |**String** <br/> |Der LCID oder BCP 47 Wert für die Sprache.  <br/> |
   
## <a name="return-value"></a>R�ckgabewert

Integer
  
## <a name="example"></a>Beispiel

 `LANGUAGE("en-us")`
  
Gibt den Wert "1033" zurück.
  
 `LANGUAGE("es-es")`
  
Gibt den Wert "3082" zurück.
  

