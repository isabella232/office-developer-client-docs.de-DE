---
title: Nachrichten Text mit TNEF-Tags
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
# <a name="tnef-tagged-message-text"></a>Nachrichten Text mit TNEF-Tags

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der getaggte Nachrichtentext wird von TNEF verwendet, um die Anlagen Positionen in der übergeordneten Nachricht aufzulösen. Dies geschieht durch Hinzufügen eines Platzhalters im Nachrichtentext an der Position der Anlage. Dieser Platzhalter oder das Attachment-Tag beschreibt die Anlage so, dass TNEF weiß, wie die Anlage und ihre Position aufgelöst werden kann. Die Tags werden wie folgt formatiert:
  
 `[[ <Object Title> : <KeyNum> in <Stream Name> ]] [[ <File Name> : <KeyNum> in <Transport Name> ]]`
  
 **Objekt Titel\> und Dateiname sind Variablen mit Werten, die aus der Anlage selbst entnommen werden. \<** **\> \<** In Fällen, in denen diese Werte nicht verfügbar sind, wird der Titel von TNEF basierend auf dem Anlagentyp standardmäßig verwendet. 
  
Die ** \<KeyNum\> ** -Variable enthält die Textdarstellung des Anlagen Schlüssels, der der Anlage von TNEF zugewiesen wurde. Der Basiswert des Schlüssels wird an den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf übergeben. Der Basiswert darf nicht NULL sein und sollte bei jedem Aufruf von **OpenTnefStreamEx**nicht identisch sein. Es sollte ausreichen, Pseudozufallszahlen basierend auf der Systemzeit von beliebigen Zufallszahlengeneratoren ihrer Laufzeitbibliothek zu verwenden, sofern Sie sicherstellen, dass Sie niemals NULL sind.
  
Die ** \<Variable Transport\> Name** enthält entweder den Streamnamen, der an den [OpenTnefStreamEx](opentnefstreamex.md) -Aufruf übergeben wird, oder den Wert der **PR_ATTACH_TRANSPORT_NAME** ([pidtagattachtransportname (](pidtagattachtransportname-canonical-property.md))-Eigenschaft.
  
> [!NOTE]
> Die **PR_ATTACH_TRANSPORT_NAME** -Eigenschaft und die ** \<Transport\> Name** -Variable in einem Nachrichten texttag haben nichts mit dem Namen des Transportanbieters zu tun, den Sie implementieren. Diese Elemente stellen den Namen einer Anlage für den Transportanbieter und das Messagingsystem dar. 
  
Der Nachrichtentext wird gekennzeichnet, wenn ein Transportanbieter einen markierten Nachrichtentext durch Aufrufen der [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode anfordert. Beim Lesen aus dem markierten Textstream ersetzt TNEF das einzelne Zeichen, das sich im Nachrichtentext des in der **PR_RENDERING_POSITION** ([pidtagrenderingposition (](pidtagrenderingposition-canonical-property.md))-Eigenschaft angegebenen Index befand, durch das entsprechende Tag. Beim Schreiben in den getaggten Textstream prüft TNEF die eingehenden Daten nach Tags, sucht die zugehörige Anlage und ersetzt das Tag durch ein einzelnes Leerzeichen.
  
Beachten Sie, dass ein Transportanbieter mithilfe des markierten Nachrichtentexts die Positionierung von Anlagen unabhängig von den meisten am Nachrichtentext durch Messagingsysteme vorgenommenen Änderungen beibehalten kann.
  

