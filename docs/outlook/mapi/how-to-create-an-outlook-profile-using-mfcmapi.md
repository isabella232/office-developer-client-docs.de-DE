---
title: Erstellen eines Outlook-Profils mit MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von problemen Exchange und Outlook zu erleichtern und Entwicklern Unterstützung für die MAPI-Entwicklung zu bieten.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345990"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Erstellen eines Outlook-Profils mit MFCMAPI

MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von problemen Exchange und Outlook zu erleichtern und Entwicklern Unterstützung für die MAPI-Entwicklung zu bieten.

**Gilt für**: Office 365 | Outlook | Outlook 2016 
  
Für Nichtentwickler wird empfohlen, die benutzeroberfläche Outlook zum Erstellen von Profilen für Exchange 2013 zu verwenden.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Konfigurieren eines Outlook mithilfe von MFCMAPI

1. Öffnen [Sie MFCMAPI,](https://mfcmapi.codeplex.com/)und klicken Sie im Menü **Profil** auf **Profile anzeigen.** 
    
2. Klicken Sie **im** Menü Aktionen auf **Profil erstellen.** 
    
3. Erstellen Sie einen neuen Namen für das Profil, und klicken Sie dann auf **OK**. 
    
4. Klicken Sie mit der rechten Maustaste  auf das neue Profil, und klicken Sie dann im Menü Dienste auf **Dienst hinzufügen.** 
    
5. Deaktivieren Sie das Kontrollkästchen Dienstbenutzeroberfläche anzeigen, und klicken Sie dann auf **OK**. 
    
6. Doppelklicken Sie auf das neu erstellte Profil, und klicken Sie dann auf den **MSEMS-Dienst.** 
    
7. Suchen Sie den Exchange Profil.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Sie benötigen diesen Wert in Schritt 9.
    
8. Doppelklicken Sie auf den **MSEMS-Dienst.** 
    
9. Suchen Sie **Exchange** Profilabschnitt mithilfe der UID aus Schritt 7, und klicken Sie dann mit einem Klick auf die Zeile. 
    
10. Klicken Sie im Menü Eigenschaft auf **Zusätzliche Eigenschaften**. 
    
11. Klicken **Sie auf** Hinzufügen , und fügen Sie dann die folgenden Eigenschaften hinzu: 
    
    **For Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` and`PR_DISPLAY_NAME_W`
    
    **For Outlook for Office 365**: `PR_PROFILE_UNRESOLVED_NAME` , `PR_PROFILE_UNRESOLVED_SERVER` , , , `PR_ROH_PROXY_SERVER` , `PR_ROH_FLAGS` , `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` and`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **For Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME` , , , , , , and `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Klicken **Sie auf OK,** und konfigurieren Sie dann jede Eigenschaft gemäß der folgenden Tabelle, je nach version, mit der Sie eine Verbindung herstellen. 
    
13. Klicken Sie **im** Menü Sitzung auf **Logon and Display Store**, und wählen Sie dann das Profil aus (wenn es noch nicht ausgewählt ist). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Tag** <br/> |**Beschreibung** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-Adresse des Benutzers  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Der Anzeigename des Benutzers  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Konfigurieren Sie den Wert dieser Eigenschaft im Abschnitt **EMSMDB,** und aktualisieren Sie die entsprechende UID für die übereinstimmende Eigenschaft.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook für Office 365
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfachalias  <br/> |Der Alias für das Zielpostfach; z. B. Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-ID  <br/> |Der aus der **AutoErmittlung abgerufene Wert.** im Format <guid> @tenant.onmicrosoft.com, z. B. F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlungsknoten*  : Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *AutoErmittlungsknoten*  : Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über Http (Hypertext Transfer Protocol) verwendet wird. *AutoErmittlungsknoten*  : Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Represents the authentication protocol to be used for this profile *AutoDiscover Node*  : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Beschreibt das für den *RPC-AutoErmittlungsknoten*  zu verwendende Authentifizierungsschema : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName-Element  <br/> |Wird verwendet, um die gegenseitige Authentifizierung zu unterstützen. beispiel: msstd:outlook.com *AutoErmittlungsknoten*  : Response/Account/Protocol/CertPrincipalName (EXPR) ) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfachalias  <br/> |Der Alias für das Zielpostfach; z. B. Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-ID  <br/> |Der aus der **AutoErmittlung abgerufene Wert.** im Format <guid> @tenant.onmicrosoft.com, z. B. F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlungsknoten*  : Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | Clientzugriffsserverdomänenname  <br/> | Der vollqualifizierte Domänenname (FQDN); Beispiel: e2013cas.contoso.com  *AutoErmittlungsknoten*  : Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über den *AutoErmittlungsknoten* Hypertext Transfer Protocol (HTTP) verwendet wird: Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Represents the authentication protocol to be used for this profile *AutoDiscover Node*  : Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Beschreibt das für den *RPC-AutoErmittlungsknoten*  zu verwendende Authentifizierungsschema : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Alle oben genannten Eigenschaftswerte können für Ihre bestimmte Organisation variieren. 
> - <sup>1</sup> Sie müssen die Unicode-Version anstelle der ANSI-Version verwenden. 
> - Sie müssen die poX-basierte AutoErmittlung (Plain Old XML) verwenden. Dies ist die einzige unterstützte AutoErmittlung zum Konfigurieren von Outlook/Exchange-Profilen.
> - Sie können Outlook verwenden, um eine AutoErmittlungsanforderung in Ihrem Namen zu erstellen, indem Sie im **Systemfach** mit der rechten Maustaste auf das Outlook-Symbol klicken, während Sie STRG gedrückt halten und auf Autokonfiguration für **E-Mail testen klicken.** 
> - Für PR_ROH_FLAGS ihre Umgebung möglicherweise das Flag ROHFLAGS_SSL_ONLY (0x2), damit MAPI nur SSL verwenden darf. Wenn Ihre Umgebung eine gegenseitige Authentifizierung erfordert, müssen Sie auch dieses Flag [ROHFLAGS_MUTUAL_AUTH (0x4)] festlegen. Für ROHFLAGS_MUTUAL_AUTH (0x4) müssen Sie auch die Eigenschaft PR_ROH_PROXY_PRINCIPAL_NAME. Sie sollten festlegen, dass dies der Prinzipalname des Servers ist.
> - <sup>2</sup> Für Outlook 2010 müssen Sie das EXPR-Protokoll verwenden. Outlook 2013 verwendet das EXHTTP-Protokoll. 
> - <sup>3</sup> Dieser Wert ist möglicherweise nicht in der AutoErmittlungsantwort. Wenn nicht angegeben, sollte der Client Kerberos oder NTLM verwenden. 
    
Tipps zur Problembehandlung finden Sie unter [Konfigurieren eines Outlook-Profils mithilfe von MFCMAPI für Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Referenz für Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Programmgesteuertes Erstellen eines Profils in Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

