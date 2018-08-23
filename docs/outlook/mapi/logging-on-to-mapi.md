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
ms.openlocfilehash: 63f71066b1afc90c3e495ed4f9ba654bcbdfe558
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579928"
---
# <a name="logging-on-to-mapi"></a>Anmelden bei MAPI
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Clientanwendungen melden Sie sich an den MAPI-Subsystems durch Aufrufen der Funktion **MAPILogonEx** . Weitere Informationen finden Sie unter [MAPILogonEx](mapilogonex.md). **MAPILogonEx** überprüft die Profilauswahl und die Konfiguration der einzelnen-Dienstanbieter im Profil. Nach der Konfiguration, startet MAPI der adressbuchanbietern implementierte vor dem Starten der Nachricht-Anbieter. Transportanbieter gestartet wurden, wenn ihre Dienste zuerst benötigt werden. 
  
## <a name="choose-a-profile"></a>Wählen Sie ein Profil
  
- Übergeben Sie eine Zeichenfolge, die den Namen des Profils im Parameter _LpszProfileName_ **MAPILogonEx**, darstellt oder...
    
- Ermöglicht es dem Benutzer das Profil, NULL in der _LpszProfileName_ -Parameter übergeben wird und die Kennzeichen MAPI_LOGON_UI angeben oder... 

- Wählen Sie das Standardprofil durch NULL im _LpszProfileName_ -Parameter übergeben, und das MAPI_USE_DEFAULT-Flag festlegen. 
    
Wenn Sie ein bestimmtes Profil als Standardprofil benötigen, müssen Sie deren Namen in Ihrer eigenen Konfigurationsdatenbank speichern oder eine spezielle Benennungskonvention verwenden. MAPI macht keine Profilattribute als das Flag Name und die Standardwerte in der Profiltabelle, und die Standard-Profil-Flag ist für die messaging-Client und zugehörige IPM Applikationen reserviert.
  
Clients, die teilweise Profil oder Anbieter-Konfigurationsinformationen zu **MAPILogonEx** bereitstellen müssen den Benutzer für die zusätzlichen Daten auffordern, durch Zulassen der ein Dialogfeld angezeigt werden. Wenn Informationen fehlen und **MAPILogonEx** kann nicht der Benutzer aufgefordert, ihn angeben, schlägt die Anmeldung. Clients, die keine Notwendigkeit von Benutzereingaben nicht ausführen, können das Dialogfeld Feld Display unterdrücken. 
  
Die Kennzeichen, die **MAPILogonEx** verwendet, um eine Benutzeroberfläche aktivieren schließen sich gegenseitig aus; nur kann festgelegt werden. Diese Flags nicht festgelegte verlassen unterdrückt die Anzeige einer Benutzeroberfläche, wodurch **MAPILogonEx** fehlschlagen, wenn die erforderlichen Informationen nicht vorhanden ist. D. h., wenn Sie die Benutzeroberfläche deaktivieren und übergeben Sie NULL für den Parameter _LpszProfileName_ , Sie die Kennzeichen MAPI_USE_DEFAULT nicht legen fehl **MAPILogonEx** , da er einen Profilnamen nicht abrufen kann. 
  
Die Sitzung, die **MAPILogonEx** richtet kann ein einzelnes messaging-Sitzung, einen freigegebenen messaging-Sitzung oder eine nonmessaging Sitzung sein. Einzelne messaging Sitzungen sind VPN-Verbindungen zwischen dem Client und MAPI-Subsystems und können durch Festlegen des MAPI_NEW_SESSION-Flags im Aufruf **MAPILogonEx**hergestellt werden.
  
Freigegebene messaging-Sitzungen werden Verbindungen, die mehrere messaging-Clients verwenden können. Freigegebene Sitzungen sind für die Verwendung durch Clients des gleichen Profils in der Regel eingerichtet. Um eine neue Sitzung als freigegebenen Sitzung herzustellen, legen Sie das MAPI_ALLOW_OTHERS-Flag. 
  
## <a name="use-an-existing-shared-session"></a>Verwenden Sie eine vorhandene freigegebene Sitzung
  
- Das Flag MAPI_NEW_SESSION nicht festgelegt.
    
- Das Flag MAPI_ALLOW_OTHERS nicht festgelegt.
    
- Übergeben Sie NULL für den Parameter _LpszProfileName_ . 
    
- Übergeben Sie NULL für den Parameter _LpszPassword_ . 
    
Nonmessaging Sitzungen ermöglichen Clients das MAPI-Subsystem zugreifen, aber Nachrichten gesendet oder empfangen wurden nicht zulassen. Konfiguration oder Verwaltung Applikationen sind Beispiele für Clients, die möglicherweise nonmessaging Sitzungen herstellen. Um eine nonmessaging Sitzung anzufordern, legen Sie das MAPI_NO_MAIL-Flag. Wenn Sie dieses Flag anmeldet Ihrer Client ohne informiert die MAPI-Warteschlange. Clients, die mit diesem Flag MAPI anmelden können nicht erwarten jemals lesen Statusberichte.
  
Das Flag MAPI_NO_MAIL sollte nur festgelegt werden:
  
- Wenn der Client wird nicht senden oder Empfangen von Nachrichten während der Sitzung.
    
- Wenn der Client hat die vollständige Kontrolle über den Inhalt des Profils und Nachrichten gesendet und Empfangen von eng gekoppelten Nachrichtenspeicher und transport-Anbieter, wie die Microsoft Exchange-Anbieter.
    
Messaging-Client kann eine Sitzung mit einem nonmessaging Client freigeben. Die Merkmale eines Elements einer freigegebenen Sitzung werden die Merkmale der anderen Elemente nicht betroffen. D. h., wenn Sie sich mit dem Flags MAPI_NO_MAIL und MAPI_ALLOW_OTHERS anmelden, wirkt sich ein messaging-Client anmelden, die Sitzung nicht auf den Vorgang des Clients und umgekehrt. Der messaging-Client wird weiterhin in der Lage, senden und Empfangen von Nachrichten und der Client aber nicht.
  
**MAPILogonEx** definiert ein paar Flags, die festgelegt werden können: 
  
- MAPI_FORCE_DOWNLOAD gibt an, dass eingehende Nachrichten heruntergeladen werden sollen, bevor **MAPILogonEx** zurückgegeben. Nicht festlegen dieses Kennzeichen bewirkt, dass Nachrichten im Hintergrund zu einem späteren Zeitpunkt heruntergeladen werden. 
    
- MAPI_SERVICE_UI_ALWAYS fordert an, dass jede Nachricht Dienste im Profil ein Konfigurationsdialogfeld angezeigt.
    
- MAPI_NT_SERVICE gibt an, dass Ihre Clients als Windows-Dienst implementiert wird. Dieses Kennzeichen müssen festgelegt werden, wenn der Client einen Dienst handelt.
    
Mit jeder erfolgreichen Anmeldung gibt **MAPILogonEx** einen Zeiger auf eine MAPI-Sitzung. Sie können diese Zeiger zum Aufrufen der Methoden der **IMAPISession** -Schnittstelle verwenden. Weitere Informationen finden Sie unter [IMAPISession: IUnknown](imapisessioniunknown.md). Sitzung Zeigern, unabhängig von der Art der Sitzung, gelten nur für Clients, die empfangen werden und sind mehrere Vorgänge nicht gültig.
  

