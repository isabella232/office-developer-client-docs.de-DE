---
title: Registrieren von Diensten und Dienstanbietern in MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: a04acf17-4b2d-458e-9852-b6074acac096
description: 'Last modified: July 18, 2013'
ms.openlocfilehash: 89d3307cfe685247fae8ec4f2bbebf46bf32d0b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599123"
---
# <a name="registering-services-and-service-providers-in-mapisvcinf"></a>Registrieren von Diensten und Dienstanbietern in MapiSvc.inf

 
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Zum Installieren eines neuen Anbieters auf einem System muss die Datei MapiSvc.inf aktualisiert werden, um auf den neuen Anbieter zu verweisen. Standardeigenschaften, die während der Konfiguration festgelegt werden, einschließlich der folgenden, informieren die MAPI darüber, wo sie die Dynamic Link Library (.dll) des Anbieters finden kann:
  
- Die **PR_SERVICE_DLL_NAME** wird im Abschnitt **[Nachrichtendienst]** angegeben. 
    
- Die **PR_PROVIDER_DLL_NAME** wird im Abschnitt **[Dienstanbieter]** angegeben. 
    
> [!NOTE]
> Es wird erwartet, dass Sie den Namen des .dll Ihres Anbieters festlegen (ohne das Suffix "32"). MAPI lädt dann Ihren Anbieter, indem sie im Pfad nach ihm sucht. 
  
## <a name="putting-a-path-in-mapisvcinf"></a>Einfügen eines Pfads in MapiSvc.inf

Die meisten Anwendungen werden unter "Programmdateien" installiert, sodass eine Aktualisierung der Pfadvariable erforderlich ist, damit MAPI-Anbieter funktionieren können. Mit einigen Einschränkungen können Microsoft Outlook 2010 und Outlook 2013 vollständige Pfade zu MAPI-Anbietern berücksichtigen.
  
Bei der Registrierung Ihres Anbieters in MapiSvc.inf können Sie den vollständigen Pfad zum Anbieter in den MAPI-Eigenschaften **PR_SERVICE_DLL_NAME** und **PR_PROVIDER_DLL_NAME** angeben.
  
In beiden Eigenschaften muss der vollständige Pfad ohne das Suffix "32" sein, da mapi diese weiterhin an den Dateinamen anfügt, bevor sie nach Ihrer Datei sucht. Dies bedeutet, dass mapi beim Registrieren des Pfads "c:\mypath\myprovider.dll" versucht, "c:\mypath\myprovider32.dll" zu laden.
  
Da die MAPI von Outlook ursprünglich nicht für vollständige Pfade vorgesehen war, wird diese Einfügung des Suffixes "32" durchgeführt, indem nach dem ersten Punkt in der Zeichenfolge gesucht wird. Dies bedeutet, dass Pfade, die andere Punkte enthalten, nicht funktionieren, sodass Sie keine Pfade wie "c:\my.path\myprovider.dll" oder "c:\mypath\my.provider.dll" verwenden können.
  
Manchmal generieren Sie in einem Store-Anbieter Eintragsbezeichner mithilfe der **WrapStoreEntryID-Funktion,** die als Parameter den Namen Ihres Anbieters verwendet. 
  
> [!IMPORTANT]
> Wenn Sie vollständige Pfade in MapiSvc.inf verwenden, müssen Sie bei Aufrufen von **WrapStoreEntryID** denselben Pfad verwenden. 
  
Darüber hinaus kann der verwendete Pfad mithilfe der codepage, die von der [GetACP-Funktion](https://msdn.microsoft.com/library/windows/desktop/dd318070%28v=vs.85%29.aspx/) bereitgestellt wird, in und aus Unicode konvertiert werden. 
  
> [!CAUTION]
> Wenn Sie einen Pfad auswählen, der Zeichen enthält, die einen solchen Roundtrip durch die [Funktionen MultiByteToWideChar](https://msdn.microsoft.com/library/windows/desktop/dd319072%28v=vs.85%29.aspx/) und [WideCharToMultiByte](https://msdn.microsoft.com/library/windows/desktop/dd374130%28v=vs.85%29.aspx/) nicht überstehen können, tritt ein Fehler auf. 
  
Für eine Demonstration dieser Funktionalität wurde das [Umschlossene PST-Beispiel](https://github.com/stephenegriffin/Outlook2010CodeSamples) auf GitHub überarbeitet – die entsprechende Funktionalität befindet sich in **MergeWithMapiSvc** und **GenerateProviderPath.**
  

