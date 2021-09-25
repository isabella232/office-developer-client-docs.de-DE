---
title: TNEF-Tagged Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d74b1c232cefe0233f97c196a968e2feed2d3b5a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624034"
---
# <a name="tnef-tagged-message-text"></a>TNEF-Tagged Nachrichtentext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Markierter Nachrichtentext wird von TNEF verwendet, um Anlagenpositionen in der übergeordneten Nachricht aufzulösen. Dazu wird ein Platzhalter im Nachrichtentext an der Position der Anlage hinzugefügt. Dieser Platzhalter oder Anlagentag beschreibt die Anlage so, dass TNEF weiß, wie die Anlage und ihre Position aufgelöst werden. Die Tags sind wie folgt formatiert:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\<Object Title\>** und **\<File Name\>** Variablen mit Werten sind, die aus der Anlage selbst stammen. In Fällen, in denen diese Werte nicht verfügbar sind, wird der Titel basierend auf dem Anlagentyp standardmäßig von TNEF verwendet. 
  
Die **\<KeyNum\>** Variable enthält die Textdarstellung des Anlagenschlüssels, der der Anlage von TNEF zugewiesen wurde. Der Basiswert des Schlüssels wird an den [OpenTnefStreamEx-Aufruf](opentnefstreamex.md) übergeben. Der Basiswert darf nicht null sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx** identisch sein. Es sollte ausreichen, pseudozufällige Zahlen basierend auf der Systemzeit zu verwenden, unabhängig davon, welchen Zufallszahlengenerator Ihre Laufzeitbibliothek bereitstellt, solange Sie garantieren, dass sie nie Null sind.
  
Die **\<Transport Name\>** Variable enthält entweder den Streamnamen, der an den [OpenTnefStreamEx-Aufruf](opentnefstreamex.md) übergeben wird, oder den Wert der **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) -Eigenschaft.
  
> [!NOTE]
> Die **PR_ATTACH_TRANSPORT_NAME-Eigenschaft** und die **\<Transport Name\>** Variable in einem Nachrichtentexttag haben nichts mit dem Namen des Transportanbieters zu tun, den Sie implementieren. Diese Elemente stellen den Namen einer Anlage für den Transportanbieter und das Messagingsystem dar. 
  
Der Nachrichtentext wird markiert, wenn ein Transportanbieter durch Aufrufen der [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) nach einem markierten Nachrichtentext fragt. Beim Lesen aus dem markierten Textstream ersetzt TNEF das einzelne Zeichen, das sich im Nachrichtentext am Index befand, der in der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) -Eigenschaft bereitgestellt wurde, durch das entsprechende Tag. Beim Schreiben in den markierten Textdatenstrom überprüft TNEF die eingehenden Daten auf Tags, sucht die zugeordnete Anlage und ersetzt das Tag durch ein einzelnes Leerzeichen.
  
Beachten Sie, dass ein Transportanbieter mithilfe von markierten Nachrichtentext die Positionierung von Anlagen unabhängig von den meisten Änderungen beibehalten kann, die von Messagingsystemen am Nachrichtentext vorgenommen wurden.
  

