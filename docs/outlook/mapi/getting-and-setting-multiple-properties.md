---
title: Abrufen und Festlegen mehrerer Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29b7f5f1-afc1-45d9-8867-9312c072e74b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dd25751978eb036531238e6372e35934b3ec145a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432261"
---
# <a name="getting-and-setting-multiple-properties"></a>Abrufen und Festlegen mehrerer Eigenschaften

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Durch das Aufrufen und festlegen so vieler Eigenschaften wie möglich mit der geringsten Anzahl von Anrufen wird die Remote Aktivität eingeschränkt, und der mit den einzelnen Eigenschaften verbundene Aufwand wird reduziert. Obwohl Dienstanbieter versuchen, Eigenschaften zu sammeln, bevor Sie einen Remoteprozeduraufruf zum Abrufen oder ändern ausführen, können Sie diesen Aufwand optimieren, indem Sie zunächst mehrere Eigenschaften anfordern.
  
Wenn Sie beispielsweise mit Routing Listen arbeiten, die zukünftige Empfänger mit benannten Eigenschaften beschreiben, die zu bestimmten Eigenschaftensätzen gehören, verarbeiten Sie alle Empfänger mit zwei anrufen. Verwenden Sie einen Aufruf von [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) , um die Bezeichner für alle Empfänger Eigenschaften und den anderen Aufruf von [IMAPIProp::](imapiprop-getprops.md) GetProps abzurufen, um alle Werte abzurufen. Die Alternative, durch die ein Aufruf von **GetIDsFromNames** gefolgt von einem Aufruf **** von GetProps für jeden Empfänger erfolgt, ist weitaus weniger effizient. 
  

