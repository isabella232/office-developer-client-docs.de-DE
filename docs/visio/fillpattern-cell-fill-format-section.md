---
title: Zelle "FillPattern" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797011"
---
# <a name="fillpattern-cell-fill-format-section"></a>FillPattern Cell (Fill Format Section)

Legt das Füllmuster für das Shape fest. Verwenden Sie die USE-Funktion in dieser Zelle, um ein benutzerdefiniertes Füllmuster anzugeben.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Keine (transparente Füllung).  <br/> |
|1  <br/> |Einfarbige Vordergrundfarbe.  <br/> |
|2 – 40  <br/> |Verschiedene Füllmuster, die den indizierten Einträgen im Dialogfeld **Füllbereich** entsprechen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch über das Dialogfeld **Füllbereich** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Shape** auf **Füllbereich**, und klicken Sie dann auf **Füllbereichsoptionen**).
  
Wenn Sie einen Verweis auf die Zelle FillPattern aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |FillPattern  <br/> |
   
Wenn Sie einen Verweis auf die Zelle FillPattern aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillPattern** <br/> |
   

