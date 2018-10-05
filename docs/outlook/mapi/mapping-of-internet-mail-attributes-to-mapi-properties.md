---
title: Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400369"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Zuordnen von Internet-Mail-Attributen zu MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Anhang wird beschrieben, wie ein MAPI-Transportdienst oder MAPI-fähigen Gateway mit dem Internet verbunden zwischen MAPI Nachrichteneigenschaften und Simple Mail Transport Protocol (SMTP) Nachrichtenattribute übersetzen sollten. SMTP ist das messaging auf einen Großteil der im Internet verwendete Protokoll. SMTP definiert eine Reihe von Nachrichtenkopfzeilen – der Nachrichtenumschlag – und einen Content-Nachrichtenformat. SMTP ist vollständig dokumentiert, in einem Satz von zwei Dokumenten, RFC 821 und RFC 822 einer Reihe von FTP und WWW-Websites im Internet gefunden werden kann.
  
Informationen über das SMTP-Protokoll verwendet, um eine Kommunikation mit SMTP-basierte e-Mail-Agenten, finden Sie in RFC 821 "Simple Mail Transfer Protocol," unter [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Reagieren auf und standard Nachrichtenkopfzeilen finden Sie im RFC 822, "Standard für das Format von ARPA Internet-Textnachrichten," unter [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
MIME, finden Sie unter RFC 1521, "MIME (Multipurpose Internet Mail Extensions)-Teil einer: Mechanismen zum angeben und Beschreiben des Formats Internet Message Bodies" unter [https://www.rfc-editor.org](https://www.rfc-editor.org).
  
Das Ziel der Zuordnung SMTP Nachrichtenattribute zu MAPI-Eigenschaften (und umgekehrt) ist, stellen Sie sicher, dass des gesamten Inhalts der MAPI-Nachrichten über die mit systemeigenen SMTP-Nachrichtenattribute codiert werden können, zwischen verschiedenen MAPI zuverlässig ausgetauscht werden können Komponenten, die über das Internet kommunizieren müssen. Dieses Dokument basiert auf arbeiten, die bereits an eine solche Komponenten bei Microsoft. 
  
In diesem Dokument wird davon ausgegangen, gute Kenntnisse im Umgang mit MAPI-Transport, TNEF und SMTP-Mail. Es ist bestrebt, Risiken löschen, statt präzise sein.
  
Als eine Konvention "Ausgehend" verweist auf Reisen aus einem MAPI-kompatible UA oder MTA mit dem Internet mail und "eingehenden" bezieht sich auf Reisen über das Internet zu einer Komponente MAPI Mail.
  

