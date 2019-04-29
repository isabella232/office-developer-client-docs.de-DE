---
title: LANGUAGE-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Ermöglicht Vergleichsvorgänge zwischen verschiedenen sprach Darstellungen. Es wird am besten für die Konvertierung von Internet Engineering Task Force Language Tags (BCP 47)-Werten in Gebietsschema-ID (LCID)-Werte verwendet.
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424752"
---
# <a name="language-function"></a>LANGUAGE-Funktion

Ermöglicht Vergleichsvorgänge zwischen verschiedenen sprach Darstellungen. Es wird am besten für die Konvertierung von Internet Engineering Task Force Language Tags (BCP 47)-Werten in Gebietsschema-ID (LCID)-Werte verwendet.
  
## <a name="version-information"></a>Informationen zur Version

Hinzugefügte Version: Visio 2013
 
  
## <a name="syntax"></a>Syntax

 **Sprache** ( _lcid_or_bcp47_)
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _lcid_or_bcp47_ <br/> |Erforderlich  <br/> |**String** <br/> |Der LCID-oder BCP 47-Wert für die Sprache.  <br/> |
   
## <a name="return-value"></a>Rückgabewert

Ganze Zahl
  
## <a name="example"></a>Beispiel

 `LANGUAGE("en-us")`
  
Gibt den Wert "1033" zurück.
  
 `LANGUAGE("es-es")`
  
Gibt den Wert "3082" zurück.
  

