---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c36dd3e6761c5bb63fe6560bfa332d1b0548b689
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567928"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Informationen über die MAPI-MIME-Konvertierungs-API

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI-MIME-Konvertierungs-API ermöglicht E-Mail-Anbietern die Konvertierung zwischen MIME-Objekten und MAPI-Nachrichten. Es stellt Konstantendefinitionen, Klassenbezeichner und Schnittstellenbezeichner bereit, wie in [MAPI-Konstanten](mapi-constants.md)dargestellt. E-Mail-Anbieter müssen eine Instanz von **[IConverterSession](iconvertersessioniunknown.md)** erstellen, indem sie die **CoCreateInstance-Funktion** aufrufen. 
  

