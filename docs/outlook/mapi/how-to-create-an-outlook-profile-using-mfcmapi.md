---
title: Erstellen eines Outlook-Profils mit MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI (engl.) bietet Zugriff auf MAPI-Speicher um Untersuchung von Exchange und Outlook Probleme zu vereinfachen und Entwickler mit Unterstützung für die Entwicklung von MAPI bereitzustellen.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397877"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Erstellen eines Outlook-Profils mit MFCMAPI

MFCMAPI (engl.) bietet Zugriff auf MAPI-Speicher um Untersuchung von Exchange und Outlook Probleme zu vereinfachen und Entwickler mit Unterstützung für die Entwicklung von MAPI bereitzustellen.

**Gilt für**: Office 365 | Outlook | Outlook 2016 
  
Für nicht-Entwickler empfiehlt es sich für die Verwendung der Benutzeroberfläche von Outlook zum Erstellen von Profilen für Exchange 2013.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Konfigurieren eines Outlook-Profils mithilfe von MFCMAPI (engl.)

1. Öffnen Sie [MFCMAPI (engl.)](https://mfcmapi.codeplex.com/), und klicken Sie im Menü **Profile** auf **Profile anzeigen**. 
    
2. Klicken Sie im Menü **Aktionen** auf **Profil erstellen**. 
    
3. Erstellen Sie einen neuen Namen für das Profil, und klicken Sie dann auf **OK**. 
    
4. Mit der rechten Maustaste in des neuen Profils, und klicken Sie dann im Menü **Dienste** auf **Dienst hinzufügen**. 
    
5. Deaktivieren Sie das Kontrollkästchen "Display Service UI", und klicken Sie dann auf **OK**. 
    
6. Doppelklicken Sie auf das neu erstellte Profil, und klicken Sie dann auf den Dienst **MSEMS** . 
    
7. Suchen Sie den Exchange-Profil-Abschnitt.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Sie benötigen diesen Wert in Schritt 9 fort.
    
8. Doppelklicken Sie auf den Dienst **MSEMS** . 
    
9. Suchen Sie den **Exchange** -Profil-Abschnitt mithilfe der UID aus Schritt 7, und klicken Sie dann einem einzelnen Klick, um die Zeile auszuwählen. 
    
10. Klicken Sie im Menü Eigenschaft auf **Zusätzliche Eigenschaften**. 
    
11. Klicken Sie auf **Hinzufügen**, und fügen Sie die folgenden Eigenschaften: 
    
    **Für Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` und`PR_DISPLAY_NAME_W`
    
    **Für Outlook für Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`, und`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **Für Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, und `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Klicken Sie auf **OK**, und konfigurieren Sie anschließend auf jede Eigenschaft gemäß der folgenden Tabelle, je nach der Version, die eine Verbindung herstellen. 
    
13. Im Menü **Sitzung** auf **Anmeldung und Anzeige Store**, und wählen Sie das Profil (sofern es nicht bereits aktiviert ist). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Tag** <br/> |**Beschreibung** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-Adresse des Benutzers  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Der Anzeigename des Benutzers  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Konfigurieren Sie den Wert dieser Eigenschaft, befindet sich im Abschnitt **EMSMDB** und aktualisieren Sie die entsprechende UID für die übereinstimmenden-Eigenschaft  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook für Office 365
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfach-alias  <br/> |Der Alias für das Zielpostfach; beispielsweise Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-id  <br/> |Der Wert von **AutoErmittlung**abgerufen. im Format <guid>@tenant.onmicrosoft.com; beispielsweise F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlung Knoten* : Antwort/Konto/Protokoll/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.Office365.com  <br/> | *AutoErmittlung Knoten* : Antwort/Konto/Protokoll/Server (AUSDR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/> ROH_FLAGS_USE_SSL (0 X 2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0 X 4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20)  <br/> |Enthält die Einstellungen in einem Profil von Outlook verwendet werden, um mit Microsoft Exchange Server eine Verbindung über einen Remoteprozeduraufruf (RPC) über Hypertext Transfer Protocol (HTTP). *AutoErmittlung Knoten* : Antwort/Konto/Protokoll/SSL (AUSDR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0 X 1)  <br/> |Stellt das Authentifizierungsprotokoll für dieses Profil *AutoErmittlung Knoten* verwendet werden soll: Antwort/Konto/Protokoll/AuthPackage (Ausdruck) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0 X 0)  <br/> |Beschreibt das Authentifizierungsschema für den RPC- *AutoErmittlung Knoten* verwenden: Antwort/Konto/Protokoll/AuthPackage (EXCH)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName-element  <br/> |Verwendet, um die gegenseitigen Authentifizierung unterstützen. *AutoErmittlung Knoten* beispielsweise msstd:outlook.com: Antwort/Konto/Protokoll/CertPrincipalName (Ausdruck)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfach-alias  <br/> |Der Alias für das Zielpostfach; beispielsweise Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-id  <br/> |Der Wert von **AutoErmittlung**abgerufen. im Format <guid>@tenant.onmicrosoft.com; beispielsweise F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlung Knoten* : Antwort/Konto/Protokoll/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | Name des Clientzugriffsservers Domäne  <br/> | Den vollqualifizierten Domänennamen (FQDN); *AutoErmittlung Knoten* beispielsweise e2013cas.contoso.com: Antwort/Konto/Protokoll/Server (AUSDR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0 X 1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0 X 8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0 X 20))  <br/> |Enthält die Einstellungen in einem Profil von Outlook für die Verbindung mit Microsoft Exchange Server unter Verwendung einen Remoteprozeduraufruf (RPC) über Hypertext Transfer Protocol (HTTP) *Für die AutoErmittlung Knoten* verwendete: Antwort/Konto/Protokoll/SSL (AUSDR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0 X 2)  <br/> |Stellt das Authentifizierungsprotokoll für dieses Profil *AutoErmittlung Knoten* verwendet werden soll: Antwort/Konto/Protokoll/AuthPackage (Ausdruck) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0XA)  <br/> |Beschreibt das Authentifizierungsschema mit RPC- *AutoErmittlung Knoten* : Antwort/Konto/Protokoll/AuthPackage (EXCH)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Alle oben genannten Werte können für Ihre Organisation bestimmte variieren. 
> - <sup>1</sup> Sie müssen die Unicode-Version, statt die ANSI-Version verwenden. 
> - Sie müssen die einfache alte XML (POX) verwenden AutoErmittlung basiert. Dies ist die einzige unterstützte AutoErmittlung zum Konfigurieren von Outlook/Exchange-Profilen.
> - Outlook können Sie um eine autoermittlungsanforderung für die in Ihrem Auftrag zu machen, indem Sie mit der rechten Maustaste in der **Taskleiste**auf des Outlook-Symbols bei gedrückter STRG-Taste und klicken auf die **Automatische Clientkonfiguration Test-e-Mail**. 
> - Für PR_ROH_FLAGS erfordern Ihre Umgebung möglicherweise das Flag ROHFLAGS_SSL_ONLY (0 x 2) anzuweisen, MAPI, um nur SSL verwendet werden. Wenn Ihre Umgebung gegenseitigen Authentifizierung erfordert, müssen Sie auch diese Flag [ROHFLAGS_MUTUAL_AUTH (0 x 4)] festgelegt. Festlegen von ROHFLAGS_MUTUAL_AUTH (0 x 4) erforderlich, dass Sie auch die PR_ROH_PROXY_PRINCIPAL_NAME-Eigenschaft festlegen. Sie sollten auf den Prinzipalnamen des Servers festgelegt.
> - <sup>2</sup> für Outlook 2010, müssen Sie das Argument AUSDR-Protokoll verwendet werden. Outlook 2013 verwendet das EXHTTP-Protokoll. 
> - <sup>3</sup> dieser Wert möglicherweise nicht in der Antwort der AutoErmittlung. Wenn nicht angegeben ist, sollte der Client Kerberos oder NTLM verwendet. 
    
Tipps zur Problembehandlung finden Sie unter [konfigurieren ein Outlook-Profils mithilfe von MFCMAPI ERSTELLTES für Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Referenz für Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Programmgesteuertes Erstellen eines Profils in Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

