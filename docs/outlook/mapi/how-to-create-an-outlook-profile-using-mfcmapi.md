---
title: Erstellen eines Outlook-Profils mit MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von Exchange-und Outlook-Problemen zu erleichtern und Entwicklern die Unterstützung der MAPI-Entwicklung zu ermöglichen.
ms.openlocfilehash: 8a300ad53918b22cc3de5554a1e3c29289cd9365
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345990"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Erstellen eines Outlook-Profils mit MFCMAPI

MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von Exchange-und Outlook-Problemen zu erleichtern und Entwicklern die Unterstützung der MAPI-Entwicklung zu ermöglichen.

**Gilt für**: Office 365 | Outlook | Outlook 2016 
  
Für nicht-Entwickler wird empfohlen, dass Sie die Outlook-Benutzeroberfläche verwenden, um Profile für Exchange 2013 zu erstellen.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Konfigurieren eines Outlook-Profils mit MFCMAPI

1. Öffnen Sie [MfcMapi](https://mfcmapi.codeplex.com/), und klicken Sie im Menü **Profil** auf **Profile anzeigen**. 
    
2. Klicken Sie im Menü **Aktionen** auf **Profil erstellen**. 
    
3. Erstellen Sie einen neuen Namen für das Profil, und klicken Sie dann auf **OK**. 
    
4. Klicken Sie mit der rechten Maustaste auf das neue Profil, und klicken Sie dann im Menü **Dienste** auf **Dienst hinzufügen**. 
    
5. Deaktivieren Sie das Kontrollkästchen Benutzeroberfläche anzeigen, und klicken Sie dann auf **OK**. 
    
6. Doppelklicken Sie auf das neu erstellte Profil, und klicken Sie dann auf den **MSEMS** -Dienst. 
    
7. Suchen Sie den Abschnitt Exchange-Profil.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Sie benötigen diesen Wert in Schritt 9.
    
8. Doppelklicken Sie auf den **MSEMS** -Dienst. 
    
9. Suchen Sie den Abschnitt **Exchange** -Profil mithilfe der UID aus Schritt 7, und wählen Sie dann die Zeile mit einem Mausklick aus. 
    
10. Klicken Sie im Menüeigenschaft auf **Weitere Eigenschaften**. 
    
11. Klicken Sie auf **Hinzufügen**, und fügen Sie dann die folgenden Eigenschaften hinzu: 
    
    **für Outlook 2016**: `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` und`PR_DISPLAY_NAME_W`
    
    **für Outlook für Office 365**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, `PR_PROFILE_AUTH_PACKAGE`und`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **für Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME`, `PR_PROFILE_UNRESOLVED_SERVER`, `PR_ROH_PROXY_SERVER`, `PR_ROH_FLAGS`, `PR_ROH_PROXY_AUTH_SCHEME`, und `PR_PROFILE_AUTH_PACKAGE`. 
    
12. Klicken Sie auf **OK**, und konfigurieren Sie dann jede Eigenschaft gemäß der Tabelle unten, je nachdem, mit welcher Version Sie eine Verbindung herstellen. 
    
13. Klicken Sie im Menü **Sitzung** auf **Anmelde-und Anzeige Speicher**, und wählen Sie dann das Profil aus (falls es nicht bereits ausgewählt ist). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Tag** <br/> |**Beschreibung** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-Adresse des Benutzers  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Der Anzeigename des Benutzers  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Konfigurieren Sie den Wert dieser Eigenschaft im Abschnitt **EMSMDB** , und aktualisieren Sie die entsprechende UID für die passende Eigenschaft.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook für Office 365
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfach-Alias  <br/> |Der Alias für das Zielpostfach; Beispiel: Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-ID  <br/> |Der von der **AutoErmittlung**abgerufene Wert. im Format <guid>@tenant. onmicrosoft.com; Beispiel: F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Autodiscover-Knoten* : Response/Account/Protocol/Server (kurspunkt)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |Outlook.office365.com  <br/> | *Autodiscover-Knoten* : Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über Hypertext Transfer Protocol (HTTP) verwendet wird. *Autodiscover Node* : Response/Account/Protocol/SSL (expr) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Stellt das Authentifizierungsprotokoll dar, das für diesen Profil- *Auto Ermittlungs Knoten* verwendet werden soll: Response/Account/Protocol/AUTHPACKAGE (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0 festlegen)  <br/> |Beschreibt das für den RPC- *Auto Ermittlungs Knoten* zu verwendende Authentifizierungsschema: Response/Account/Protocol/AuthPackage (kurspunkt)) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName-Element  <br/> |Wird zur Unterstützung der gegenseitigen Authentifizierung verwendet. beispielsweise msstd:Outlook. com *autodiscover Node* : Response/Account/Protocol/CERTPRINCIPALNAME (expr)) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfach-Alias  <br/> |Der Alias für das Zielpostfach; Beispiel: Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |personalisierte Server-ID  <br/> |Der von der **AutoErmittlung**abgerufene Wert. im Format <guid>@tenant. onmicrosoft.com; Beispiel: F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *Autodiscover-Knoten* : Response/Account/Protocol/Server (kurspunkt)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | Domänenname des Clientzugriffsservers  <br/> | Der vollqualifizierte Domänenname (FQDN); beispielsweise e2013cas.contoso.com *autodiscover Node* : Response/Account/Protocol/Server (expr) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über Hypertext Transfer Protocol (HTTP) *autodiscover Node* : Response/Account/Protocol/SSL (expr) <sup>2</sup> verwendet wird. <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Stellt das Authentifizierungsprotokoll dar, das für diesen Profil- *Auto Ermittlungs Knoten* verwendet werden soll: Response/Account/Protocol/AUTHPACKAGE (expr) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Beschreibung des für den RPC- *Auto Ermittlungs Knoten* zu verwendenden Authentifizierungsschemas: Response/Account/Protocol/AuthPackage (kurspunkt)) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Alle oben aufgeführten Eigenschaftswerte können für Ihre Organisation unterschiedlich sein. 
> - <sup>1</sup> Sie müssen die Unicode-Version anstelle der ANSI-Version verwenden. 
> - Sie müssen die einfache alte XML (POX)-basierte AutoErmittlung verwenden. Dies ist die einzige unterstützte AutoErmittlung zum Konfigurieren von Outlook/Exchange-Profilen.
> - Sie können Outlook verwenden, um eine autoErmittlungs-Anforderung in Ihrem Namen zu erstellen, indem Sie mit der rechten Maustaste auf das Outlook-Symbol in der Task **Leiste**klicken, während Sie die STRG-Taste gedrückt halten und dann auf **e-Mail-Test** 
> - Für PR_ROH_FLAGS kann für Ihre Umgebung das Flag ROHFLAGS_SSL_ONLY (0x2) erforderlich sein, um MAPI mitzuteilen, dass nur SSL verwendet werden soll. Wenn für Ihre Umgebung die gegenseitige Authentifizierung erforderlich ist, müssen Sie dieses Flag auch [ROHFLAGS_MUTUAL_AUTH (0x4)] festlegen. Wenn Sie ROHFLAGS_MUTUAL_AUTH (0x4) festlegen, müssen Sie auch die PR_ROH_PROXY_PRINCIPAL_NAME-Eigenschaft festlegen. Sie sollten dies als Prinzipalnamen des Servers festlegen.
> - <sup>2</sup> für Outlook 2010 müssen Sie das expr-Protokoll verwenden. Outlook 2013 verwendet das HTTP-Protokoll. 
> - <sup>3</sup> dieser Wert ist möglicherweise nicht in der AutoErmittlung-Antwort. Wenn nicht angegeben, sollte der Client Kerberos oder NTLM verwenden. 
    
Tipps zur Problembehandlung finden Sie unter [Konfigurieren eines Outlook-Profils mit MfcMapi für Exchange 2013](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Referenz für Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Programmgesteuertes Erstellen eines Profils in Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

