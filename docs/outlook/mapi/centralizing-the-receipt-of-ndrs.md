---
title: Zentral verwalten den Empfang von Unzustellbarkeitsberichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0af587bd07de9445f143be316798059eaef402e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791405"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Zentral verwalten den Empfang von Unzustellbarkeitsberichten

**Betrifft**: Outlook 
  
**Eintreffen damit Unzustellbarkeitsberichten (NDR) an einem zentralen Speicherort, wenn mehrere Instanzen Ihres Clients gleichzeitig ausgeführt werden**
  
1. Legen Sie die entsprechenden Werte für das Konto, das erhalten **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) die Berichte. Erstellen Sie die Eintrags-ID durch Aufrufen von [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) bei Bedarf. 
    
2. Erkennen Sie, dass die messaging-Systemen, die das Konto für Berichte angefordert haben und diese an den Absender senden ignoriert werden. Reduzieren Sie die Auswirkungen mit dies auf Administratoren, die Berichte durch bewegen müssen:
    
- Wenn Sie für Ihre ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse wie IPM. Note.MSNNews. Suchen Sie nach eingehende Nachrichten mit Report.IPM.Note.MSNNews.NDR-Klasse und Notizen an dasselbe Konto wie gewünscht Berichte zu betrachten. Gleichzeitig senden Sie e-Mail an die messaging-System, das ignoriert Ihr Konto Nondelivery Bericht, um anzuzeigen, ob es die **PR_REPORT_ENTRYID** -Eigenschaft berücksichtigt werden sollten. 
    
- Die meisten Messagingsysteme, die berücksichtigt **PR_REPORT_ENTRYID** nicht berücksichtigt die MAPI-Nachricht Klasse Konventionen nicht entweder. Aus diesem Grund erhalten etwas Sie, die eine Notiz aussieht. Dies ist etwas schwieriger zu bewältigen, da die Eingabe also Variable ist. Sehen Sie sich den Betreff und Weiterleiten Sie, wenn Sie entweder etwas aus einer Liste von Wörtern, Mittelwert "unzustellbar" oder etwas aus Ihrer ursprünglichen Betreff finden. Seien Sie diese Listen über einen Zeitraum zu optimieren. 
    

