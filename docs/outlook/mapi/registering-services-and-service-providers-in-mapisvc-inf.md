---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc. inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Zuletzt geändert: 18, 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328371"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrieren von Diensten und Dienstanbietern in MapiSvc. inf

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Für die Installation eines neuen Anbieters auf einem System muss die Datei MapiSvc. inf aktualisiert werden, damit auf den neuen Anbieter verwiesen wird. Standard Eigenschaften, die während der Konfiguration festgelegt werden, einschließlich der folgenden, informieren Sie MAPI, wo die Dynamic-Link-Bibliothek des Anbieters (dll) zu finden ist:
  
- Die **PR_SERVICE_DLL_NAME** wird im Abschnitt **[Message Service]** angegeben. 
    
- Die **PR_PROVIDER_DLL_NAME** wird im Abschnitt **[Service Provider]** angegeben. 
    
> [!NOTE]
> Es wird davon ausgegangen, dass Sie den Namen der dll Ihres Anbieters (ohne Suffix "32") festlegen. MAPI lädt dann Ihren Anbieter, indem er nach dem Pfad sucht. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Einfügen eines Pfads in MapiSvc. inf

Die meisten Anwendungen werden Unterprogramm Dateien installiert, wobei eine Aktualisierung der PATH-Variablen erforderlich ist, damit MAPI-Anbieter arbeiten können. Mit einigen Einschränkungen können Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbietern aufnehmen.
  
Wenn Sie Ihren Anbieter in MapiSvc. inf registrieren, können Sie den vollständigen Pfad zum Anbieter in den MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**.
  
In beiden Eigenschaften muss der vollständige Pfad ohne das Suffix "32" sein, da MAPI die Datei weiterhin an den Dateinamen anhängt, bevor Sie nach Ihrer Daten sucht. Wenn Sie also den Pfad "c:\mypath\myprovider.dll" registrieren, versucht MAPI, "c:\mypath\myprovider32.dll" zu laden.
  
Da die MAPI von Outlook ursprünglich nicht für vollständige Pfade konzipiert wurde, führt Sie diese Einfügung des Suffixes "32" durch, indem Sie nach dem ersten Punkt in der Zeichenfolge sucht, was heißt, dass Pfade, die andere Punkte enthalten, nicht funktionieren können, sodass Sie keine Pfade wie "c:\My.path\myprovider.dll" oder "c:\mypath\my.Provider.dll".
  
Manchmal werden Sie in einem Informationsspeicher Anbieter Eingabe-IDs mithilfe der **WrapStoreEntryID** -Funktion generieren, die als Parameter den Namen Ihres Anbieters verwendet. 
  
> [!IMPORTANT]
> Wenn Sie in MapiSvc. inf vollständige Pfade verwenden, müssen Sie den gleichen Pfad in allen Aufrufen von **WrapStoreEntryID**verwenden. 
  
Darüber hinaus kann der verwendete Pfad mithilfe der Codeseite, die von der [GetACP](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) -Funktion bereitgestellt wird, in und aus Unicode konvertiert werden. 
  
> [!CAUTION]
> Wenn Sie einen Pfad auswählen, der Zeichen enthält, die einen solchen Roundtrip über die [MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) -und [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) -Funktionen nicht überstehen können, tritt ein Fehler auf. 
  
Für eine Demonstration dieser Funktionalität wurde das [Wrapped PST-Beispiel](https://github.com/stephenegriffin/Outlook2010CodeSamples) auf GitHub überarbeitet – die entsprechende Funktionalität befindet sich in **MergeWithMapiSvc** und **GenerateProviderPath**.
  

