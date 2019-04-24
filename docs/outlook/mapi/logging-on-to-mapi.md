---
title: Anmelden bei MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: cce43301ac73a5646e263b2ab92700e57804637d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307777"
---
# <a name="logging-on-to-mapi"></a>Anmelden bei MAPI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Client Anwendungen melden sich beim MAPI-Subsystem an, indem Sie die **MAPILogonEx** -Funktion aufrufen. Weitere Informationen finden Sie unter [MAPILogonEx](mapilogonex.md). **MAPILogonEx** überprüft die Profilauswahl und die Konfiguration der einzelnen Dienstanbieter im Profil. Nach der Konfiguration startet MAPI die Adressbuchanbieter, bevor der Nachrichtenspeicher Anbieter gestartet wird. Transport Anbieter werden gestartet, wenn ihre Dienste zuerst erforderlich sind. 
  
## <a name="choose-a-profile"></a>Profil auswählen
  
- Übergeben Sie eine Zeichenfolge, die den Namen des Profils im _lpszProfileName_ -Parameter darstellt **MAPILogonEx**, oder...
    
- Geben Sie dem Benutzer die Möglichkeit, das Profil anzugeben, indem Sie im _lpszProfileName_ -Parameter den Wert NULL übergeben und das MAPI_LOGON_UI-Flag festlegen. 

- Wählen Sie das Standardprofil aus, indem Sie im _lpszProfileName_ -Parameter den Wert NULL übergeben und das MAPI_USE_DEFAULT-Flag festlegen. 
    
Wenn Sie ein anderes Profil als das Standardprofil benötigen, müssen Sie den Namen in ihrer eigenen Konfigurationsdatenbank speichern oder eine bestimmte Benennungskonvention verwenden. MAPI stellt keine anderen Profilattribute als den Namen und das Standardkennzeichen in der Profiltabelle zur Verfügung, und das standardmäßige Profil Kennzeichen ist für den Messaging Client und die zugehörigen IPM-Anwendungen reserviert.
  
Clients, die Teilprofil-oder Anbieter Konfigurationsinformationen für **MAPILogonEx** bereitstellen, müssen den Benutzer für die zusätzlichen Daten auffordern, indem ein Dialogfeld angezeigt wird. Wenn Informationen fehlen und **MAPILogonEx** den Benutzer nicht zur Verfügung stellen kann, schlägt die Anmeldung fehl. Clients, die keine Benutzereingabe benötigen, können die Anzeige des Dialogfelds unterdrücken. 
  
Die Flags, die **MAPILogonEx** verwendet, um eine Benutzeroberfläche zu aktivieren, schließen sich gegenseitig aus; Es kann nur eine festgelegt werden. Wenn Sie diese Flags verlassen, wird die Anzeige einer Benutzeroberfläche unterdrückt, sodass **MAPILogonEx** fehlschlägt, wenn erforderliche Informationen fehlen. Das heißt, wenn Sie die Benutzeroberfläche deaktivieren und NULL für den _lpszProfileName_ -Parameter übergeben und das MAPI_USE_DEFAULT-Flag nicht festlegen, schlägt **MAPILogonEx** fehl, da ein Profilname nicht abgerufen werden kann. 
  
Bei der **MAPILogonEx** -Sitzung kann es sich um eine einzelne Messaging Sitzung, eine freigegebene Messaging Sitzung oder eine nonmessaging-Sitzung handeln. Einzelne Messagingsitzungen sind private Verbindungen zwischen dem Client und dem MAPI-Subsystem und können durch Festlegen des MAPI_NEW_SESSION-Kennzeichens im Aufruf an **MAPILogonEx**festgelegt werden.
  
FreigeGebene Messagingsitzungen sind Verbindungen, die von mehreren Messagingclients verwendet werden können. FreigeGebene Sitzungen werden in der Regel für Clients eingerichtet, die das gleiche Profil verwenden. Legen Sie das MAPI_ALLOW_OTHERS-Flag fest, um eine neue Sitzung als freigegebene Sitzung einzurichten. 
  
## <a name="use-an-existing-shared-session"></a>Verwenden einer vorhandenen freigegebenen Sitzung
  
- Legen Sie das MAPI_NEW_SESSION-Flag nicht fest.
    
- Legen Sie das MAPI_ALLOW_OTHERS-Flag nicht fest.
    
- Übergeben Sie NULL für den _lpszProfileName_ -Parameter. 
    
- Übergeben Sie NULL für den _lpszPassword_ -Parameter. 
    
Nonmessaging-Sitzungen ermöglichen Clients den Zugriff auf das MAPI-Subsystem, lassen jedoch keine Nachrichten senden oder empfangen. Konfigurations-oder Verwaltungsanwendungen sind Beispiele für Clients, die möglicherweise nonmessaging-Sitzungen erstellen müssen. Legen Sie das MAPI_NO_MAIL-Flag fest, um eine nonmessaging-Sitzung anzufordern. Durch Festlegen dieses Kennzeichens wird der Client protokolliert, ohne dass der MAPI-Spooler informiert wird. Clients, die sich mit diesem Flag bei MAPI anmelden, können nicht erwarten, dass Sie jemals Lesestatus Berichte erhalten.
  
Das MAPI_NO_MAIL-Flag sollte nur festgelegt werden:
  
- Wenn Ihr Client während der Sitzung keine Nachrichten senden oder empfangen wird.
    
- Wenn Ihr Client die vollständige Kontrolle über die Inhalte des Profils hat und Nachrichten mit eng gekoppelten Nachrichtenspeicher-und Transportanbietern, beispielsweise den Microsoft Exchange-Anbietern, gesendet und empfangen werden.
    
Ein Messaging Client kann eine Sitzung mit einem nicht-Messaging-Client gemeinsam nutzen. Die Merkmale eines Members einer freigegebenen Sitzung sind von den Merkmalen anderer Mitglieder nicht betroffen. Wenn Sie sich also mit der MAPI_NO_MAIL-und der MAPI_ALLOW_OTHERS-Flags-Gruppe anmelden, hat ein Messaging-Client, der sich an ihrer Sitzung anmeldet, keine Auswirkung auf den Betrieb Ihres Clients und umgekehrt. Der Messaging Client ist weiterhin in der Lage, Nachrichten zu senden und zu empfangen, und der Client nicht.
  
**MAPILogonEx** definiert einige andere Flags, die Sie festlegen können: 
  
- MAPI_FORCE_DOWNLOAD gibt an, dass eingehende Nachrichten heruntergeladen werden sollen, bevor **MAPILogonEx** zurückgegeben wird. Wenn Sie dieses Flag nicht festlegen, werden Nachrichten zu einem späteren Zeitpunkt im Hintergrund heruntergeladen. 
    
- MAPI_SERVICE_UI_ALWAYS fordert, dass jeder Nachrichtendienst im Profil ein Konfigurationsdialogfeld anzeigt.
    
- MAPI_NT_SERVICE gibt an, dass Ihr Client als Windows-Dienst implementiert ist. Dieses Flag muss festgelegt werden, wenn Ihr Client ein Dienst ist.
    
Bei jeder erfolgreichen Anmeldung gibt **MAPILogonEx** einen Zeiger auf eine MAPI-Sitzung zurück. Sie können diesen Zeiger verwenden, um die Methoden der **IMAPISession** -Schnittstelle aufzurufen. Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md). Sitzungs Zeiger, unabhängig vom Sitzungstyp, sind für die Clients eindeutig, die Sie empfangen und für alle Aufgaben nicht gültig sind.
  

