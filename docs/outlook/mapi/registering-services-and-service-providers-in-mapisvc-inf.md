---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Letzte Änderung: 18. Juli 2013'
ms.openlocfilehash: adc6318ab36818b4c423bb6b1dc1b083b3fb54eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328371"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrieren von Diensten und Dienstanbietern in MapiSvc.inf

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Für die Installation eines neuen Anbieters auf einem System muss die Datei MapiSvc.inf so aktualisiert werden, dass sie auf den neuen Anbieter zeigt. Standardeigenschaften, die während der Konfiguration festgelegt werden, z. B. die folgenden, informieren MAPI darüber, wo die Dynamic-Link-Bibliothek des Anbieters (.dll):
  
- Die **PR_SERVICE_DLL_NAME** wird im **Abschnitt [Nachrichtendienst]** angegeben. 
    
- Die **PR_PROVIDER_DLL_NAME** wird im **Abschnitt [Dienstanbieter]** angegeben. 
    
> [!NOTE]
> Es wird erwartet, dass Sie den Namen des Anbieternamens .dll (ohne das Suffix "32") festlegen. MAPI lädt dann Ihren Anbieter, indem Sie ihn auf dem Pfad suchen. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Pfad in MapiSvc.inf

Die meisten Anwendungen werden unter Programmdateien installiert und erfordern ein Update der Pfadvariablen, damit MAPI-Anbieter funktionieren können. Mit einigen Einschränkungen können Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbietern aufnehmen.
  
Beim Registrieren Ihres Anbieters in MapiSvc.inf können Sie den vollständigen Pfad zum Anbieter in den MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME**.
  
In beiden Eigenschaften muss der vollständige Pfad ohne das Suffix "32" sein, da MAPI dies weiterhin an den Dateinamen anfügen muss, bevor sie nach Ihrer Datei sucht. Dies bedeutet, dass MAPI beim Registrieren des Pfads "c:\mypath\myprovider.dll" versucht, "c:\mypath\myprovider32.dll".
  
Da die MAPI von Outlook ursprünglich nicht für vollständige Pfade vorgesehen war, wird das Suffix "32" eingefügt, indem nach dem ersten Zeitraum in der Zeichenfolge gesucht wird, was bedeutet, dass Pfade, die andere Zeiträume enthalten, nicht funktionieren können, sodass Pfade wie "c:\my.path\myprovider.dll" oder "c:\mypath\my.provider.dll" nicht verwendet werden können.
  
Manchmal generieren Sie in einem Speicheranbieter Eintragsbezeichner mit der **WrapStoreEntryID-Funktion,** die als Parameter den Namen Ihres Anbieters annimmt. 
  
> [!IMPORTANT]
> Wenn Sie vollständige Pfade in MapiSvc.inf verwenden, müssen Sie bei Aufrufen von **WrapStoreEntryID denselben Pfad verwenden.** 
  
Darüber hinaus kann der von Ihnen verwendete Pfad mithilfe der Codeseite, die von der [GetACP-Funktion](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) bereitgestellt wird, in Unicode und von Unicode konvertiert werden. 
  
> [!CAUTION]
> Wenn Sie einen Pfad auswählen, der Zeichen enthält, die einen solchen Roundtrip durch die [Funktionen MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) und [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) nicht überstehen können, wird ein Fehler gemacht. 
  
Für eine Demonstration dieser Funktionalität wurde das Umbrochene [PST-Beispiel](https://github.com/stephenegriffin/Outlook2010CodeSamples) auf GitHub überarbeitet – die entsprechenden Funktionen finden Sie in **MergeWithMapiSvc** und **GenerateProviderPath**.
  

