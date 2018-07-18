---
title: TNEF-markierter Nachrichtentext
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8c65339e-240c-412d-9b71-69c746468bfb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bedfc0457b0de8287a4e7bc8bdf8fb57404e4fa8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795739"
---
# <a name="tnef-tagged-message-text"></a>TNEF-markierter Nachrichtentext

  
  
**Betrifft**: Outlook 
  
Markierte des Nachrichtentexts wird von TNEF zum Anlage Positionen in der übergeordneten Nachricht zu beheben. Dies erfolgt durch ein Platzhalter im Nachrichtentext an der Position der Anlage hinzufügen. Dieser Platzhalter oder ein Attachment-Tag beschreibt die Anlage in einer Weise, dass TNEF weiß, wie Sie das Attachment-Objekt und seine Position auflösen können. Die Tags sind wie folgt formatiert:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 ** \<Objekt Titel\> ** und ** \<Dateinamen\> ** sind Variablen, die mit den Werten, die aus der Anlage selbst ausgeführt werden. In Fällen, in dem diese Werte nicht verfügbar sind, wird der Titel von TNEF basierend auf den Anlagetyp übernommen. 
  
Die ** \<KeyNum\> ** Variable enthält die Textdarstellung des Schlüssels Anlage, die die Anlage durch TNEF zugewiesen. Der Basiswert des Schlüssels übergeben wird in den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf. Der Basiswert darf nicht NULL sein und sollte nicht für jeden Aufruf von **OpenTnefStreamEx**identisch sein. Es reicht, um basierend auf der Systemzeit aus den Zufallszahlengenerator Ihrer Laufzeitbibliothek bereitstellt, solange Sie sicherstellen, dass sie nie NULL sind Pseudo-Zufallszahlen zu verwenden.
  
Die ** \<Transport Namen\> ** Variable enthält entweder den Stream Namen in der [OpenTnefStreamEx](opentnefstreamex.md) -Anruf oder der Wert der Eigenschaft **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) übergeben.
  
> [!NOTE]
> Die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaft und die ** \<Transport Namen\> ** Variable in einem Text-Tag Nachricht haben nichts tun mit dem Namen des Anbieters Transport Sie implementieren. Diese Elemente stellen den Namen der Anlage für den Transportdienst und messaging-System. 
  
Der Nachrichtentext gekennzeichnet ist, wenn für einen markierten Text ein Transportdienstes auffordert, durch die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode aufrufen. Beim Lesen aus dem markierten Textstream ersetzt TNEF das einzelne Zeichen, das im Nachrichtentext im Index in der Eigenschaft **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) mit dem entsprechenden Tag bereitgestellt wurde. Beim Schreiben in den markierten Textstream TNEF überprüft die eingehenden Daten für Tags zugeordnete Anlage gesucht und ersetzt das Tag durch ein einzelnes Leerzeichen.
  
Beachten Sie, dass mithilfe des Nachrichtentexts markierte ein Transportdienstes die Positionierung von Anlagen unabhängig von den meisten Änderungen an den Nachrichtentext beibehalten kann von messaging-Systeme.
  

