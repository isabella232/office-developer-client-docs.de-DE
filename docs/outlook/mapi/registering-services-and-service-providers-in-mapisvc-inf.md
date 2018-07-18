---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Zuletzt geändert: 18 Juli 2013'
ms.openlocfilehash: 2eb7f1b496e0732b157ea4f9105a0e067329c52f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795359"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrieren von Diensten und Dienstanbietern in MapiSvc.inf

 
  
**Betrifft**: Outlook 
  
Installieren einen neuen Anbieter auf einem System erfordert die Aktualisierung der Datei "MapiSvc.inf" So zeigen Sie auf den neuen Anbieter. Standardeigenschaften festlegen während der Konfiguration, die Folgendes enthalten, MAPI zu informieren, wo der Anbieter Dynamic Link Library (DLL) zu finden:
  
- Die **PR_SERVICE_DLL_NAME** wird im Abschnitt **[Messagingdiensts]** angegeben. 
    
- Die **PR_PROVIDER_DLL_NAME** wird im Abschnitt **[Service Provider]** angegeben. 
    
> [!NOTE]
> Es wird erwartet, dass Sie den Namen des Anbieters DLL (ohne das Suffix "32") festgelegt. MAPI lädt Ihres Anbieters klicken Sie dann auf den Pfad gesucht. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Einen Pfad Websitemigration MapiSvc.inf

Die meisten installieren unter Programmdateien, erfordern ein Update zur Path-Variablen um MAPI-Anbieter arbeiten zu ermöglichen. Mit einigen Einschränkungen unterstützen Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbieter.
  
Beim Registrieren des Anbieters in MapiSvc.inf, könnten Sie den vollständigen Pfad des Anbieters in der MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**einfügen.
  
In beiden-Eigenschaft muss der vollständige Pfad ohne das Suffix "32", sein, da MAPI weiterhin, die an den Dateinamen anfügen, bevor Sie nach der Datei sucht. Dies bedeutet, dass wenn Sie den Pfad "c:\mypath\myprovider.dll" registrieren, MAPI versucht, "c:\mypath\myprovider32.dll" zu laden.
  
Da Outlook MAPI wurde nicht ursprünglich für vollständige Pfade ein entwickelt, sie erreicht diese Einfügung des "32" Suffixes Schlüsseltokens für den ersten Zeitraum in der Zeichenfolge, was bedeutet, dass Pfade mit anderen Perioden arbeiten können, so dass Pfade wie verwendet werden können "c:\my.path\myprovider.dll" oder "c:\mypath\my.provider.dll".
  
In einigen Fällen in einem Speicheranbieter generieren Sie mithilfe der **WrapStoreEntryID** -Funktion, die als Parameter den Namen Ihres Anbieters akzeptiert Eintragsbezeichner. 
  
> [!IMPORTANT]
> Wenn Sie vollständige Pfade in MapiSvc.inf verwenden, müssen Sie denselben Pfad in etwaigen Aufrufen **WrapStoreEntryID**verwenden. 
  
Darüber hinaus kann der Pfad, den Sie verwenden in und aus Unicode mithilfe der von der Funktion [GetACP](http://msdn.microsoft.com/en-us/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) bereitgestellte Codepage konvertiert werden soll. 
  
> [!CAUTION]
> Sie werden Fehler bemerken, wenn Sie einen Pfad auswählen, der Zeichen enthält, die eine solche eine Schleife durch die Funktionen [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) und [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) überstehen kann nicht. 
  
Für diese Funktionalität veranschaulicht im [Beispiel umgebrochen PST](http://ol2010mapisamples.codeplex.com/) auf CodePlex wurde überarbeitet – die relevante Funktionalität in **MergeWithMapiSvc** und **GenerateProviderPath**ist.
  

