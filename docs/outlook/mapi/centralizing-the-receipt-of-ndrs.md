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
  
**Wenn mehrere Instanzen des Clients gleichzeitig ausgeführt werden, werden Unzustellbarkeitsberichte an einem zentralen Ort eingetroffen.**
  
1. Legen Sie **PR_REPORT_ENTRYID** ([Pidtagreportentryid (](pidtagreportentryid-canonical-property.md)) **, PR_REPORT_NAME** ([pidtagreportname (](pidtagreportname-canonical-property.md)) und **PR_REPORT_SEARCH_KEY** ([pidtagreportsearchkey (](pidtagreportsearchkey-canonical-property.md)) auf die entsprechenden Werte für das zu empfangende Konto fest. die Berichte. Erstellen Sie die Eintrags-ID, indem Sie [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) aufrufen, falls erforderlich. 
    
2. Beachten Sie, dass es Messagingsysteme gibt, die das Konto, das Sie für Berichte angefordert haben, ignorieren und an den Absender senden. Reduzieren Sie die Auswirkungen auf Administratoren, die Berichte verschieben müssen:
    
- Geben Sie Ihrer ursprünglichen Nachricht eine unterschiedliche Nachrichtenklasse wie IPM. Hinweis. MSNNews. Suchen Sie nach eingehenden Nachrichten mit der Klasse Report. IPM. Note. MSNNews. NDR, und leiten Sie Sie an das Konto weiter, zu dem Sie Berichte erstellen möchten. Senden Sie gleichzeitig eine e-Mail an das Messagingsystem, das Ihr Unzustellbarkeitsbericht Konto ignoriert hat, um zu kommunizieren, dass die **PR_REPORT_ENTRYID** -Eigenschaft berücksichtigt werden sollte. 
    
- Die meisten Messagingsysteme, die **PR_REPORT_ENTRYID** nicht honorieren, werden die MAPI-Nachrichtenklassen Konventionen nicht berücksichtigen. Daher erhalten Sie etwas, das wie eine Notiz aussieht. Dies ist ein wenig schwieriger zu bewältigen, da die Eingabe so variabel ist. Sehen Sie sich das Thema an, und leiten Sie es weiter, wenn Sie entweder etwas aus einer Liste von Wörtern finden, die "unzustellbar" oder etwas aus Ihrem ursprünglichen Betreff bedeuten. Sie sollten diese Listen im Laufe der Zeit optimieren. 
    

