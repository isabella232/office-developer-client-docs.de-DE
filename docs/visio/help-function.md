---
title: HELP-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
ms.localizationpriority: medium
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Öffnet eine HTML-Hilfedatei mit dem angegebenen Schlüsselwort im Suchfeld.
ms.openlocfilehash: a4243a9ddbcfda7ef327efd108e1f9954c0fb7b1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618882"
---
# <a name="help-function"></a>HELP-Funktion

Öffnet eine HTML-Hilfedatei mit dem angegebenen *Schlüsselwort* im **Suchfeld.** 
  
## <a name="syntax"></a>Syntax

HELP(" ** *filename.chm!keyword* ** ") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _filename.chm!schlüsselwort_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Hilfedatei und das Stichwort, nach dem gesucht werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn kein  *Schlüsselwort*  angegeben ist, öffnet die HELP-Funktion die Inhaltsseite der Hilfedatei. 
  
## <a name="example"></a>Beispiel

HELP("visio.chm!shapesheet") 
  
Öffnet die Visio-Hilfedatei und zeigt eine Liste der Themen zum Stichwort "Shapesheet" an. 
  

