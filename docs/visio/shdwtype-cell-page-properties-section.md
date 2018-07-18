---
title: Zelle "ShdwType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Gibt den Standardschattentyp eines Zeichenblatts an.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798090"
---
# <a name="shdwtype-cell-page-properties-section"></a>ShdwType Cell (Page Properties Section)

Gibt den Standardschattentyp eines Zeichenblatts an.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 1  <br/> | Einfach  <br/> |**visFSTSimple** <br/> |
| 2  <br/> | Schräg  <br/> |**visFSTOblique** <br/> |
|3  <br/> |Innere  <br/> |**visFSTInner** <br/> |
   
## <a name="remarks"></a>Bemerkungen

 In dieser Zelle beschriebene Schattentyp wird verwendet, wenn die Zelle ShapeShdwType (der Schattentyp für ein einzelnes Shape auf der Seite) auf Seitenstandard (**VisFSTPageDefault** ) festgelegt ist. 
  
Einfacher Schatten werden als Offset Schatten auf der Benutzeroberfläche (UI) beschrieben. Ein einfacher Schatten hat den Effekt der Form wird auf eine parallele Ebene hinter werfen schattiert. Schräge Schatten werden als schräge Schatten auf der Benutzeroberfläche beschrieben, und weisen Sie die Auswirkung des einen Schatten auf eine senkrecht zum Shape. 
  
Eine Liste vordefinierter einfacher und schräger Schattentypen finden Sie im Dialogfeld **Seite einrichten** auf der Registerkarte **Schatten** in der Liste **Formatvorlage** (klicken Sie dazu auf der Registerkarte **Entwurf** auf den Pfeil neben **Seite einrichten**). 
  
Wenn Sie einen Verweis auf die Zelle ShdwType aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShdwType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageShdwType** <br/> |
   

