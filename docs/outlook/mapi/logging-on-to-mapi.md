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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419709"
---
# <a name="logging-on-to-mapi"></a>Anmelden bei MAPI
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen melden sich beim MAPI-Subsystem an, indem sie die **MAPILogonEx-Funktion** aufrufen. Weitere Informationen finden Sie unter [MAPILogonEx](mapilogonex.md). **MAPILogonEx** überprüft die Profilauswahl und die Konfiguration der einzelnen Dienstanbieter im Profil. Nach der Konfiguration startet MAPI die Adressbuchanbieter, bevor die Nachrichtenspeicheranbieter gestartet werden. Transportanbieter werden gestartet, wenn ihre Dienste zum ersten Mal benötigt werden. 
  
## <a name="choose-a-profile"></a>Auswählen eines Profils
  
- Übergeben Sie eine Zeichenzeichenfolge, die den Namen des Profils im  _lpszProfileName-Parameter_ an **MAPILogonEx** darstellt, oder...
    
- Zulassen, dass der Benutzer das Profil durch Übergeben von NULL im  _lpszProfileName-Parameter_ und Festlegen des MAPI_LOGON_UI oder... 

- Wählen Sie das Standardprofil aus, indem Sie NULL im  _lpszProfileName-Parameter_ übergeben und MAPI_USE_DEFAULT festlegen. 
    
Wenn Sie ein anderes profil als das Standardprofil benötigen, müssen Sie den Namen in Ihrer eigenen Konfigurationsdatenbank speichern oder eine bestimmte Benennungskonvention verwenden. MAPI macht keine anderen Profilattribute als den Namen und das Standardflag in der Profiltabelle verfügbar, und das Standardprofilflag ist für Messagingclients und verwandte IPM-Anwendungen reserviert.
  
Clients, die **MAPILogonEx** Teilprofil- oder Anbieterkonfigurationsinformationen zur Verfügung stellen, müssen den Benutzer zur Eingabe zusätzlicher Daten aufgefordert, indem sie die Anzeige eines Dialogfelds zulassen. Wenn Informationen fehlen und **MAPILogonEx** den Benutzer nicht zur Eingabe anforderen kann, schlägt die Anmeldung fehl. Clients, die keine Benutzereingabe benötigen, können die Anzeige des Dialogfelds unterdrücken. 
  
Die Flags, die **MAPILogonEx** zum Aktivieren einer Benutzeroberfläche verwendet, schließen sich gegenseitig aus. es kann nur eins festgelegt werden. Wenn diese Flags nicht markiert werden, wird die Anzeige einer Benutzeroberfläche unterdrückt, sodass **MAPILogonEx** fehlschlagen kann, wenn erforderliche Informationen fehlen. Wenn Sie also die Benutzeroberfläche deaktivieren und NULL für den  _lpszProfileName-Parameter_ übergeben und das MAPI_USE_DEFAULT-Flag nicht festlegen, kann **MAPILogonEx** keinen Profilnamen abrufen. 
  
Die von **MAPILogonEx** einrichtende Sitzung kann eine einzelne Messagingsitzung, eine freigegebene Messagingsitzung oder eine Nichtmessagingsitzung sein. Einzelne Messagingsitzungen sind private Verbindungen zwischen Ihrem Client und dem MAPI-Subsystem und können durch Festlegen des MAPI_NEW_SESSION im Aufruf von **MAPILogonEx eingerichtet werden.**
  
Freigegebene Messagingsitzungen sind Verbindungen, die von mehreren Messagingclients verwendet werden können. Freigegebene Sitzungen werden in der Regel für Clients eingerichtet, die dasselbe Profil verwenden. Um eine neue Sitzung als freigegebene Sitzung zu erstellen, legen Sie das MAPI_ALLOW_OTHERS fest. 
  
## <a name="use-an-existing-shared-session"></a>Verwenden einer vorhandenen freigegebenen Sitzung
  
- Legen Sie das Flag MAPI_NEW_SESSION.
    
- Legen Sie das Flag MAPI_ALLOW_OTHERS.
    
- Übergeben Sie NULL für den _lpszProfileName-Parameter._ 
    
- Übergeben Sie NULL für den _lpszPassword-Parameter._ 
    
Nichtmessing-Sitzungen ermöglichen Clients den Zugriff auf das MAPI-Subsystem, aber nicht das Senden oder Empfangen von Nachrichten. Konfigurations- oder Verwaltungsanwendungen sind Beispiele für Clients, die möglicherweise Nichtmessagingsitzungen einrichten müssen. Legen Sie zum Anfordern einer Nichtmessaging-Sitzung das MAPI_NO_MAIL ein. Durch Festlegen dieses Kennzeichens wird der Client protokolliert, ohne den MAPI-Spooler zu informieren. Clients, die sich bei MAPI mit diesem Flag anmelden, können nicht erwarten, dass sie jemals Lesestatusberichte erhalten.
  
Das MAPI_NO_MAIL flag sollte nur festgelegt werden:
  
- Wenn Ihr Client während der Sitzung keine Nachrichten sendet oder erhält.
    
- Wenn Ihr Client die vollständige Kontrolle über den Inhalt des Profils hat und Nachrichten mit eng gekoppelten Nachrichtenspeicher- und Transportanbietern, wie z. B. microsoft Exchange empfangen werden.
    
Ein Messagingclient kann eine Sitzung für einen nichtmessing-Client freigeben. Die Merkmale eines Mitglieds einer freigegebenen Sitzung werden nicht von den Merkmalen anderer Mitglieder beeinflusst. Das heißt, wenn Sie sich mit den festgelegten MAPI_NO_MAIL- und MAPI_ALLOW_OTHERS-Flags anmelden, hat die Anmeldung eines Messagingclients bei Ihrer Sitzung keine Auswirkungen auf den Clientbetrieb und umgekehrt. Der Messagingclient kann weiterhin Nachrichten senden und empfangen, der Client nicht.
  
**MAPILogonEx** definiert einige weitere Flags, die Sie festlegen können: 
  
- MAPI_FORCE_DOWNLOAD gibt an, dass eingehende Nachrichten heruntergeladen werden sollen, bevor **MAPILogonEx zurückgegeben** wird. Wenn Sie dieses Kennzeichen nicht festlegen, werden Nachrichten zu einem späteren Zeitpunkt im Hintergrund heruntergeladen. 
    
- MAPI_SERVICE_UI_ALWAYS, dass für jeden Nachrichtendienst im Profil ein Konfigurationsdialogfeld angezeigt wird.
    
- MAPI_NT_SERVICE gibt an, dass Ihr Client als Dienst Windows ist. Dieses Flag muss festgelegt werden, wenn Ihr Client ein Dienst ist.
    
Bei jeder erfolgreichen Anmeldung gibt **MAPILogonEx einen** Zeiger auf eine MAPI-Sitzung zurück. Mit diesem Zeiger können Sie die Methoden der **IMAPISession-Schnittstelle** aufrufen. Weitere Informationen finden Sie unter [IMAPISession : IUnknown](imapisessioniunknown.md). Sitzungszeiger sind unabhängig vom Sitzungstyp für die Clients, die sie empfangen, eindeutig und sind aufgabenübergreifend ungültig.
  

