---
title: Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355818"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>Zuordnung von Internet-Mail-Attributen zu MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In diesem Anhang wird beschrieben, wie ein MAPI-Transportanbieter oder EIN -MAPI-benachrichtigungsgateway, das eine Verbindung mit dem Internet herstellt, zwischen DENI-Nachrichteneigenschaften und SMTP-Nachrichtenattributen (Simple Mail Transport Protocol) übersetzt werden soll. SMTP ist das Messagingprotokoll, das in einem großen Teil des Internets verwendet wird. SMTP definiert eine Reihe von Nachrichtenkopfzeilen – den Nachrichtenumschlag – und ein Nachrichteninhaltsformat. SMTP ist vollständig in zwei Dokumenten dokumentiert, RFC 821 und RFC 822, die auf einer Reihe von FTP- und WWW-Websites im Internet zu finden sind.
  
Informationen zum SMTP-Protokoll, das für die Kommunikation mit SMTP-basierten E-Mail-Agents verwendet wird, finden Sie unter RFC 821, "Simple Mail Transfer Protocol", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Informationen zu Adressierung und Standardnachrichtenkopfzeilen finden Sie unter RFC 822, "Standard for the Format of ARPA Internet Text Messages", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Mime finden Sie unter RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies", unter [https://www.rfc-editor.org](https://www.rfc-editor.org) .
  
Das Ziel der Zuordnung von SMTP-Nachrichtenattributen zu MAPI-Eigenschaften (und umgekehrt) besteht in der Sicherstellung, dass der vollständige Inhalt von MAPI-Nachrichten, der über den Inhalt hinaus, der mit systemeigenen SMTP-Nachrichtenattributen codiert werden kann, zuverlässig zwischen verschiedenen MAPI-Komponenten ausgetauscht werden kann, die über das Internet kommunizieren müssen. Dieses Dokument basiert auf der Arbeit, die bereits an solchen Komponenten bei Microsoft durchgeführt wurde. 
  
In diesem Dokument wird die Vertrautheit mit MAPI-Transporten, TNEF und SMTP-E-Mails vorausgesetzt. Sie ist bestrebt, prägnant und nicht überdünslich klar zu sein.
  
Als Konvention bezieht sich "ausgehend" auf E-Mails, die von einem MAPI-kompatiblen UA oder MTA in das Internet reisen, und "eingehenden" auf E-Mails, die aus dem Internet zu einer MAPI-Komponente reisen.
  

