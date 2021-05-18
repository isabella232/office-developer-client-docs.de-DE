---
title: Zentralisieren des Empfangs von NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405856"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Zentralisieren des Empfangs von NDRs

**Gilt für**: Outlook 2013 | Outlook 2016 
  
**So müssen Nicht-Löschberichte (Nondelivery Reports, NDRs) an einem zentralen Ort eintreffen, wenn mehrere Instanzen Ihres Clients gleichzeitig ausgeführt werden**
  
1. Legen **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) auf die entsprechenden Werte für das Konto fest, das die Berichte empfangen soll. Erstellen Sie die Eintrags-ID, indem Sie bei Bedarf [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) aufrufen. 
    
2. Verstehen Sie, dass es Messagingsysteme gibt, die das konto ignorieren, das Sie für Berichte angefordert haben, und diese an den Ermittler senden. Verringern Sie die Auswirkungen, die dies auf Administratoren hat, die Berichte verschieben müssen, indem Sie:
    
- Geben Sie Ihrer ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse, z. B. IPM. Note.MSNNews. Suchen Sie nach eingehenden Nachrichten mit der Klasse Report.IPM.Note.MSNNews.NDR, und weiterleiten Sie sie an das Konto, zu dem Berichte kommen sollen. Senden Sie gleichzeitig E-Mails an das Messagingsystem, das Ihr Nicht-Löschbericht-Konto **ignoriert** hat, um zu kommunizieren, dass es die eigenschaft PR_REPORT_ENTRYID sollte. 
    
- Die meisten Messagingsysteme, die keine **PR_REPORT_ENTRYID,** werden auch die Konventionen der MAPI-Nachrichtenklasse nicht einhalten. Daher erhalten Sie etwas, das wie eine Notiz aussieht. Dies ist etwas schwieriger zu umgehen, da die Eingabe so variabel ist. Sehen Sie sich den Betreff an, und geben Sie ihn weiter, wenn Sie entweder etwas aus einer Liste von Wörtern finden, die "nicht zustellbar" oder etwas von Ihrem ursprünglichen Betreff bedeuten. Bereiten Sie sich darauf vor, diese Listen im Laufe der Zeit zu optimieren. 
    

