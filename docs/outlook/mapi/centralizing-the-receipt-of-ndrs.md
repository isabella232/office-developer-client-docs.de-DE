---
title: Zentralisieren des Empfangs von NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9df0229a34e26dc0a40b6405a53b71421f79d877
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551814"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Zentralisieren des Empfangs von NDRs

**Gilt für**: Outlook 2013 | Outlook 2016 
  
**Damit Nichtzustellbarkeitsberichte (NonDelivery Reports, NDRs) an einem zentralen Ort eintreffen, wenn mehrere Instanzen Ihres Clients gleichzeitig ausgeführt werden**
  
1. Legen Sie **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) auf die entsprechenden Werte für das Konto fest, das die Berichte empfangen soll. Erstellen Sie den Eintragsbezeichner, indem Sie [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) bei Bedarf aufrufen. 
    
2. Verstehen Sie, dass es Messagingsysteme gibt, die das Konto ignorieren, das Sie für Berichte angefordert haben, und diese an den Absender senden. Verringern Sie die Auswirkungen, die dies auf Administratoren hat, die Berichte verschieben müssen, indem Sie:
    
- Geben Sie ihrer ursprünglichen Nachricht eine eigene Nachrichtenklasse, z. B. IPM. Note.MSNNews. Suchen Sie nach eingehenden Nachrichten mit der Klasse Report.IPM.Note.MSNNews.NDR, und leiten Sie sie an das Konto weiter, an das Sie Berichte senden möchten. Senden Sie gleichzeitig eine E-Mail an das Messagingsystem, das Ihr Konto für den Nichtzustellbarkeitsbericht ignoriert hat, um zu kommunizieren, dass es die **eigenschaft PR_REPORT_ENTRYID** berücksichtigen soll. 
    
- Die meisten Messagingsysteme, die **PR_REPORT_ENTRYID** nicht berücksichtigen, berücksichtigen auch nicht die Konventionen der MAPI-Nachrichtenklasse. Daher erhalten Sie etwas, das wie eine Notiz aussieht. Dies ist etwas schwieriger zu verarbeiten, da die Eingabe so variabel ist. Sehen Sie sich das Thema an, und leiten Sie es weiter, wenn Sie entweder etwas aus einer Liste von Wörtern finden, die "unerstellbar" bedeuten, oder etwas aus Ihrem ursprünglichen Betreff. Bereiten Sie sich darauf vor, diese Listen im Laufe der Zeit zu optimieren. 
    

