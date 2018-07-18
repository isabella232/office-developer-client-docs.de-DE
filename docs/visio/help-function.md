---
title: HELP-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251436
localization_priority: Normal
ms.assetid: 5b358c38-6ed1-3fbe-c1d1-1a56ebbaa870
description: Öffnet eine HTML-Hilfedatei mit dem Schlüsselwort angegeben, in das Feld Suchen.
ms.openlocfilehash: 4671b18333bdae953c487662cd880849233df7f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797145"
---
# <a name="help-function"></a>HELP-Funktion

Öffnet eine HTML-Hilfedatei mit dem angegebenen *Schlüsselwort* im Feld **Suchen** . 
  
## <a name="syntax"></a>Syntax

Hilfe ("** *filename.chm!keyword* **") 
  
### <a name="parameters"></a>Parameter

|**Name**|**Erforderlich/Optional**|**Datentyp**|**Beschreibung**|
|:-----|:-----|:-----|:-----|
| _filename.chm!Keyword_ <br/> |Erforderlich  <br/> |**String** <br/> | Der Name der Hilfedatei und das Stichwort, nach dem gesucht werden soll.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn kein *Keyword* angegeben wurde, wird die HELP-Funktion die Inhaltsübersicht der Hilfedatei geöffnet. 
  
## <a name="example"></a>Beispiel

Help("Visio.chm!ShapeSheet") 
  
Öffnet die Visio-Hilfedatei und zeigt eine Liste der Themen zum Stichwort "Shapesheet" an. 
  

