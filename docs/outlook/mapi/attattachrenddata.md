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
ms.openlocfilehash: a006c126ec5e0fb86847226195efd03f7ae5351f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569449"
---
# <a name="attattachrenddata"></a>attAttachRenddata

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Das Attribut **AttAttachRenddata** wird als eine **RENDDATA** Struktur codiert, die beschreibt, wie und, in dem die Anlage im Nachrichtentext gerendert wird. Die Struktur **RENDDATA** ist einfach in der TNEF-Stream als beginnend mit dem ersten Element in der Struktur **RENDDATA** **sizeof(RENDDATA)** -Bytes codiert. Wenn der Wert der **RENDDATA** -Struktur **DwFlags** Members auf **MAC_BINARY**festgelegt ist, werden die Daten für die folgenden Anlage im MacBinary-Format gespeichert. Andernfalls werden die Anlagendaten wie gewohnt codiert.
  

