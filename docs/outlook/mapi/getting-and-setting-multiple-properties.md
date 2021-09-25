---
title: Abrufen und Festlegen mehrerer Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c15cee3268f78ee718fecf4fbdbc8b424e745372
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551548"
---
# <a name="getting-and-setting-multiple-properties"></a>Abrufen und Festlegen mehrerer Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Durch das Abrufen und Festlegen so vieler Eigenschaften wie möglich mit der geringsten Anzahl von Aufrufen wird die Remoteaktivität eingeschränkt, und der Aufwand für jede Eigenschaft wird reduziert. Obwohl Dienstanbieter versuchen, Eigenschaften zu sammeln, bevor sie einen Remoteprozeduraufruf zum Abrufen oder Ändern durchführen, können Sie diesen Aufwand optimieren, indem Sie zunächst mehrere Eigenschaften anfordern.
  
Wenn Sie beispielsweise mit Routinglisten arbeiten, die zukünftige Empfänger mit benannten Eigenschaften beschreiben, die zu bestimmten Eigenschaftensätzen gehören, verarbeiten Sie alle Empfänger mit zwei Aufrufen. Verwenden Sie einen Aufruf von [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md) um die Bezeichner für alle Empfängereigenschaften abzurufen, und den anderen Aufruf von [IMAPIProp::GetProps,](imapiprop-getprops.md) um alle Werte abzurufen. Die Alternative, einen Aufruf von **GetIDsFromNames** gefolgt von einem Aufruf von **GetProps** für jeden Empfänger, ist viel weniger effizient. 
  

