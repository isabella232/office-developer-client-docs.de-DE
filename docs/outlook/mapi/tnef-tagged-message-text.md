---
title: TNEF-Tagged Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b4d4cd790870a024cac6f2ed9952d18a970235a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419919"
---
# <a name="tnef-tagged-message-text"></a>TNEF-Tagged Nachrichtentext

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Markierter Nachrichtentext wird von TNEF zum Auflösen von Anlagenpositionen in der übergeordneten Nachricht verwendet. Dazu wird ein Platzhalter im Nachrichtentext an der Position der Anlage hinzugefügt. Dieser Platzhalter oder Anlagentag beschreibt die Anlage so, dass TNEF weiß, wie die Anlage und ihre Position aufgelöst werden. Die Tags sind wie folgt formatiert:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **\< Objekttitel \>** **\< und \> Dateiname** sind Variablen, die Werte enthalten, die aus der Anlage selbst übernommen werden. In Fällen, in denen diese Werte nicht verfügbar sind, wird der Titel standardmäßig von TNEF basierend auf dem Anlagentyp verwendet. 
  
Die **\< KeyNum-Variable \>** enthält die Textdarstellung des Anlagenschlüssels, der der Anlage von TNEF zugewiesen wurde. Der Basiswert des Schlüssels wird an den [OpenTnefStreamEx-Aufruf](opentnefstreamex.md) übergeben. Der Basiswert darf nicht null sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx gleich sein.** Es sollte ausreichen, Pseudozufallszahlen basierend auf der Systemzeit aus dem zufallszahlengenerator zu verwenden, den Ihre Laufzeitbibliothek bietet, solange Sie garantieren, dass sie nie null sind.
  
Die **\< Variable \> Transport Name** enthält entweder den An den [OpenTnefStreamEx-Aufruf](opentnefstreamex.md) übergebenen Streamnamen oder den Wert der PR_ATTACH_TRANSPORT_NAME ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) **-Eigenschaft.**
  
> [!NOTE]
> Die **PR_ATTACH_TRANSPORT_NAME-Eigenschaft** und die **\< \> Transportname-Variable** in einem Nachrichtentexttag haben nichts mit dem Namen des Transportanbieters zu tun, den Sie implementieren. Diese Elemente stellen den Namen einer Anlage für den Transportanbieter und das Messagingsystem dar. 
  
Der Nachrichtentext wird markiert, wenn ein Transportanbieter nach einem markierten Nachrichtentext fragt, indem er die [ITnef::OpenTaggedBody-Methode](itnef-opentaggedbody.md) aufruft. Beim Lesen aus dem markierten Textdatenstrom ersetzt TNEF das einzelne Zeichen, das sich im Nachrichtentext im Index in der **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))-Eigenschaft befindet, durch das entsprechende Tag. Beim Schreiben in den markierten Textdatenstrom überprüft TNEF die eingehenden Daten auf Tags, sucht die zugeordnete Anlage und ersetzt das Tag durch ein einzelnes Leerzeichen.
  
Beachten Sie, dass ein Transportanbieter mithilfe von markierten Nachrichtentext die Positionierung von Anlagen unabhängig von den meisten Änderungen am Nachrichtentext durch Messagingsysteme beibehalten kann.
  

