---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a21f6ca242f07abf865885794cf71f0ff3135eba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605174"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **AttAttachRenddata-Attribut** wird als **RENDDATA-Struktur** codiert, die beschreibt, wie und wo die Anlage im Nachrichtentext gerendert wird. Die **RENDDATA-Struktur** wird einfach im TNEF-Datenstrom als **Sizeof(RENDDATA)-Bytes** codiert, beginnend mit dem ersten Element der **RENDDATA-Struktur.** Wenn der Wert des **agFlags-Elements** der **RENDDATA-Struktur** auf **MAC_BINARY** festgelegt ist, werden die Daten für die folgende Anlage im MacBinary-Format gespeichert. andernfalls werden die Anlagendaten wie gewohnt codiert.
  

