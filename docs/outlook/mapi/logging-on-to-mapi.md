---
title: Anmelden bei MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 05bafe43-a78a-4659-92f0-0b4fe444c64f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: df5bb9c117c568889af18c4fd1accd6589390d5f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579631"
---
# <a name="logging-on-to-mapi"></a>Anmelden bei MAPI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen melden sich beim MAPI-Subsystem an, indem sie die **MAPILogonEx-Funktion** aufrufen. Weitere Informationen finden Sie unter [MAPILogonEx](mapilogonex.md). **MAPILogonEx** überprüft die Profilauswahl und die Konfiguration der einzelnen Dienstanbieter im Profil. Nach der Konfiguration startet MAPI die Adressbuchanbieter, bevor die Nachrichtenspeicheranbieter gestartet werden. Transportanbieter werden gestartet, wenn ihre Dienste zum ersten Mal erforderlich sind. 
  
## <a name="choose-a-profile"></a>Auswählen eines Profils
  
- Übergeben Sie eine Zeichenfolge, die den Namen des Profils im Parameter  _lpszProfileName_ darstellt, an **MAPILogonEx** oder...
    
- Zulassen, dass der Benutzer das Profil durch Übergeben von NULL im  _Parameter lpszProfileName_ und Festlegen des MAPI_LOGON_UI Flags angibt, oder... 

- Wählen Sie das Standardprofil aus, indem Sie NULL im Parameter  _lpszProfileName_ übergeben und das flag MAPI_USE_DEFAULT festlegen. 
    
Wenn Sie ein anderes Profil als das Standardprofil benötigen, müssen Sie dessen Namen in Ihrer eigenen Konfigurationsdatenbank speichern oder eine bestimmte Benennungskonvention verwenden. MAPI macht keine anderen Profilattribute verfügbar als den Namen und das Standardflags in der Profiltabelle, und das Standardprofil-Flag ist für Messagingclients und zugehörige IPM-Anwendungen reserviert.
  
Clients, die **MAPILogonEx** Informationen zur Partiellen Profil- oder Anbieterkonfiguration bereitstellen, müssen den Benutzer zur Eingabe der zusätzlichen Daten auffordern, indem sie das Anzeigen eines Dialogfelds zulassen. Wenn Informationen fehlen und **MAPILogonEx** den Benutzer nicht zur Angabe auffordern kann, schlägt die Anmeldung fehl. Clients, die keine Benutzereingaben benötigen, können die Anzeige des Dialogfelds unterdrücken. 
  
Die Flags, die **MAPILogonEx** zum Aktivieren einer Benutzeroberfläche verwendet, schließen sich gegenseitig aus. es kann nur einer festgelegt werden. Wenn diese Flags nicht festgelegt werden, wird die Anzeige einer Benutzeroberfläche unterdrückt, sodass **MAPILogonEx** fehlschlägt, wenn erforderliche Informationen fehlen. Wenn Sie also die Benutzeroberfläche deaktivieren und NULL für den Parameter  _lpszProfileName_ übergeben und das flag MAPI_USE_DEFAULT nicht festlegen, schlägt **MAPILogonEx** fehl, da kein Profilname abgerufen werden kann. 
  
Die von **MAPILogonEx** eingerichtete Sitzung kann eine einzelne Messagingsitzung, eine freigegebene Messagingsitzung oder eine nichtmessive Sitzung sein. Einzelne Messagingsitzungen sind private Verbindungen zwischen Ihrem Client und dem MAPI-Subsystem und können durch Festlegen des MAPI_NEW_SESSION Flags im Aufruf von **MAPILogonEx** hergestellt werden.
  
Freigegebene Messagingsitzungen sind Verbindungen, die von mehreren Messagingclients verwendet werden können. Freigegebene Sitzungen werden in der Regel für Clients eingerichtet, die dasselbe Profil verwenden. Um eine neue Sitzung als freigegebene Sitzung einzurichten, legen Sie das flag MAPI_ALLOW_OTHERS fest. 
  
## <a name="use-an-existing-shared-session"></a>Verwenden einer vorhandenen freigegebenen Sitzung
  
- Legen Sie das MAPI_NEW_SESSION Flag nicht fest.
    
- Legen Sie das MAPI_ALLOW_OTHERS Flag nicht fest.
    
- Übergeben Sie NULL für den _Parameter lpszProfileName._ 
    
- Übergeben Sie NULL für den _LpszPassword-Parameter._ 
    
Nichtmessagingsitzungen ermöglichen Clients den Zugriff auf das MAPI-Subsystem, aber nicht das Senden oder Empfangen von Nachrichten. Konfigurations- oder Verwaltungsanwendungen sind Beispiele für Clients, die möglicherweise nichtmessive Sitzungen einrichten müssen. Um eine nichtmessive Sitzung anzufordern, legen Sie das MAPI_NO_MAIL Flag fest. Durch Festlegen dieses Kennzeichens wird Ihr Client angemeldet, ohne den MAPI-Spooler zu informieren. Clients, die sich bei der MAPI mit diesem Flag anmelden, können nicht erwarten, dass sie jemals Lesestatusberichte erhalten.
  
Das MAPI_NO_MAIL Flag sollte nur festgelegt werden:
  
- Wenn Ihr Client während der Sitzung keine Nachrichten sendet oder empfängt.
    
- Wenn Ihr Client die vollständige Kontrolle über den Inhalt des Profils hat und Nachrichten über eng gekoppelte Nachrichtenspeicher- und Transportanbieter wie die Microsoft Exchange-Anbieter gesendet und empfangen werden.
    
Ein Messaging-Client kann eine Sitzung mit einem Nicht-Messaging-Client teilen. Die Merkmale eines Mitglieds einer freigegebenen Sitzung werden von den Merkmalen anderer Mitglieder nicht beeinflusst. Wenn Sie sich also mit der MAPI_NO_MAIL anmelden und MAPI_ALLOW_OTHERS Flags festgelegt sind, hat die Anmeldung eines Messagingclients bei Ihrer Sitzung keine Auswirkungen auf den Betrieb Ihres Clients und umgekehrt. Der Messaging-Client kann weiterhin Nachrichten senden und empfangen, und Ihr Client nicht.
  
**MAPILogonEx** definiert einige andere Flags, die Sie festlegen können: 
  
- MAPI_FORCE_DOWNLOAD gibt an, dass eingehende Nachrichten heruntergeladen werden sollen, bevor **MAPILogonEx** zurückgegeben wird. Wenn Sie dieses Kennzeichen nicht festlegen, werden Nachrichten zu einem späteren Zeitpunkt im Hintergrund heruntergeladen. 
    
- MAPI_SERVICE_UI_ALWAYS fordert an, dass jeder Nachrichtendienst im Profil ein Konfigurationsdialogfeld anzeigt.
    
- MAPI_NT_SERVICE gibt an, dass Ihr Client als Windows Dienst implementiert ist. Dieses Kennzeichen muss festgelegt werden, wenn Ihr Client ein Dienst ist.
    
Bei jeder erfolgreichen Anmeldung gibt **MAPILogonEx** einen Zeiger auf eine MAPI-Sitzung zurück. Sie können diesen Zeiger verwenden, um die Methoden der **IMAPISession-Schnittstelle** aufzurufen. Weitere Informationen finden Sie unter [IMAPISession : IUnknown](imapisessioniunknown.md). Sitzungszeiger sind unabhängig vom Sitzungstyp für die Clients, die sie empfangen, eindeutig und für alle Aufgaben ungültig.
  

