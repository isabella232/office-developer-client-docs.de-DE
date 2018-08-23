---
title: Informationen über die MAPI-MIME-Konvertierungs-API
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: ffdfdff8-985d-35de-73b1-c34e1932cb9f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 23e68d18a6de93a99d2db32c1d93dac33d9a1225
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575266"
---
# <a name="about-the-mapi-mime-conversion-api"></a>Informationen über die MAPI-MIME-Konvertierungs-API

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die MAPI-MIME-Konvertierung-API ermöglicht es e-Mail-Anbieter für die Konvertierung zwischen MIME-Objekte und MAPI-Nachrichten. Softwareentwicklern Konstantendefinitionen Klassenbezeichner und Schnittstellenbezeichner Siehe [MAPI-Konstanten](mapi-constants.md). E-Mail-Anbieter müssen eine Instanz des **[IConverterSession](iconvertersessioniunknown.md)** durch Aufrufen der Funktion **CoCreateInstance** cocreate. 
  

