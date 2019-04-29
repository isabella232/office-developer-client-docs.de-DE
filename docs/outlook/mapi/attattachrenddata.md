---
title: attAttachRenddata
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c510b7a5-0f55-46af-bddb-40a8195a84d4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d58fc0eae5401773d28f5bbe510913ff381ade8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427136"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das **attAttachRenddata** -Attribut wird als eine **RENDDATA** -Struktur codiert, die beschreibt, wie und wo die Anlage im Nachrichtentext gerendert wird. Die **RENDDATA** -Struktur wird einfach im TNEF-Stream als **sizeof (RENDDATA)-** Byte codiert, beginnend mit dem ersten Element der **RENDDATA** -Struktur. Wenn der Wert des **dwFlags** -Elements der **RENDDATA** -Struktur auf **MAC_BINARY**festgelegt ist, werden die Daten für die folgende Anlage im MacBinary-Format gespeichert. Andernfalls werden die Anlagendaten wie üblich codiert.
  

