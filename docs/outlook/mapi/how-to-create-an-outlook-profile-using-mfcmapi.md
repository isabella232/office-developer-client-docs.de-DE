---
title: Erstellen eines Outlook-Profils mit MFCMAPI
ms.date: 05/18/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 85581bc7-2d81-46af-8836-adef39c933fc
description: MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von problemen mit Exchange und Outlook zu erleichtern und Entwicklern Unterstützung für die MAPI-Entwicklung zu bieten.
ms.openlocfilehash: 0776619fc97ee94ae557b72cf7576b9ff6b779ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610853"
---
# <a name="create-an-outlook-profile-using-mfcmapi"></a>Erstellen eines Outlook-Profils mit MFCMAPI

MFCMAPI bietet Zugriff auf MAPI-Speicher, um die Untersuchung von problemen mit Exchange und Outlook zu erleichtern und Entwicklern Unterstützung für die MAPI-Entwicklung zu bieten.

**Gilt für**: Office 365 | Outlook | Outlook 2016 
  
Nichtentwicklern wird empfohlen, die Outlook Benutzeroberfläche zum Erstellen von Profilen für Exchange 2013 zu verwenden.
  
## <a name="configure-an-outlook-profile-using-mfcmapi"></a>Konfigurieren eines Outlook Profils mit mfcmapi

1. Öffnen Sie [MFCMAPI,](https://mfcmapi.codeplex.com/)und klicken Sie im Menü **"Profil"** auf **"Profile anzeigen".** 
    
2. Klicken Sie im Menü **"Aktionen"** auf **"Profil erstellen".** 
    
3. Erstellen Sie einen neuen Namen für das Profil, und klicken Sie dann auf **OK.** 
    
4. Klicken Sie mit der rechten Maustaste auf das neue Profil, und klicken Sie dann im Menü **"Dienste"** auf **"Dienst hinzufügen".** 
    
5. Deaktivieren Sie das Kontrollkästchen "Anzeigedienst-Benutzeroberfläche", und klicken Sie dann auf **OK.** 
    
6. Doppelklicken Sie auf das neu erstellte Profil, und klicken Sie dann auf den **MSEMS-Dienst.** 
    
7. Suchen Sie den Abschnitt Exchange Profil.
    
   This can be difficult in Outlook�s MAPI, since in 2010 and above there is no longer the global profile section. To find the Profile section, find the property PR_EMSMDB_SECTION_UID (0x3D150102). The value will be the GUID of the profile section persisted in binary form, which will be used in the subsequent steps. Sie benötigen diesen Wert in Schritt 9.
    
8. Doppelklicken Sie auf den **MSEMS-Dienst.** 
    
9. Suchen Sie den **Exchange** Profilabschnitt mithilfe der UID aus Schritt 7, und klicken Sie dann mit einem Einzigen Klick, um die Zeile auszuwählen. 
    
10. Klicken Sie im Menü "Eigenschaft" auf **"Zusätzliche Eigenschaften".** 
    
11. Klicken Sie auf **"Hinzufügen",** und fügen Sie dann die folgenden Eigenschaften hinzu: 
    
    **Für Outlook 2016:** `PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W (0x6641001F)` und`PR_DISPLAY_NAME_W`
    
    **Für Outlook für Office 365:**, `PR_PROFILE_UNRESOLVED_NAME` `PR_PROFILE_UNRESOLVED_SERVER` , `PR_ROH_PROXY_SERVER` , , `PR_ROH_FLAGS` , `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` und`PR_ROH_PROXY_PRINCIPAL_NAME` 
    
    **For Exchange 2013**: `PR_PROFILE_UNRESOLVED_NAME` , , , , , , and `PR_PROFILE_UNRESOLVED_SERVER` `PR_ROH_PROXY_SERVER` `PR_ROH_FLAGS` `PR_ROH_PROXY_AUTH_SCHEME` `PR_PROFILE_AUTH_PACKAGE` . 
    
12. Klicken Sie auf **"OK",** und konfigurieren Sie dann jede Eigenschaft gemäß der folgenden Tabelle, je nach Version, mit der Sie eine Verbindung herstellen. 
    
13. Klicken Sie im Menü **"Sitzung"** auf **"Anmelden" und "Store anzeigen",** und wählen Sie dann das Profil aus (sofern es noch nicht ausgewählt ist). 
    
### <a name="outlook-2016"></a>Outlook 2016
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Tag** <br/> |**Beschreibung** <br/> |
| PR_PROFILE_USER_SMTP_EMAIL_ADDRESS_W  <br/> |0x6641001F  <br/> |SMTP-Adresse des Benutzers  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |Der Anzeigename des Benutzers  <br/> |
|PR_STORE_PROVIDERS  <br/> |0x3D000102  <br/> |Konfigurieren Sie den Wert dieser Eigenschaft im **EMSMDB-Abschnitt,** und aktualisieren Sie die entsprechende UID für die übereinstimmende Eigenschaft.  <br/> |
   
### <a name="outlook-for-office-365"></a>Outlook für Office 365
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfachalias  <br/> |Der Alias für das Zielpostfach; z. B. Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |Personalisierte Server-ID  <br/> |Der aus der **AutoErmittlung** abgerufene Wert. im Format <guid> "@tenant.onmicrosoft.com", z. B. F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlungsknoten:*  Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> |outlook.office365.com  <br/> | *AutoErmittlungsknoten:*  Response/Account/Protocol/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/> ROH_FLAGS_USE_SSL (0x2)  <br/>  ROHFLAGS_MUTUAL_AUTH (0x4)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/>  ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20)  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über http (Hypertext Transfer Protocol) verwendet wird. *AutoErmittlungsknoten:*  Response/Account/Protocol/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_BASIC (0x1)  <br/> |Stellt das Authentifizierungsprotokoll dar, das für diesen *Profil-AutoErmittlungsknoten*  verwendet werden soll: Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_NONE (0x0)  <br/> |Beschreibt das für den *RPC-AutoErmittlungsknoten*  zu verwendende Authentifizierungsschema: Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
|PR_ROH_PROXY_PRINCIPAL_NAME  <br/> |CertPrincipalName-Element  <br/> |Wird zur Unterstützung der gegenseitigen Authentifizierung verwendet. z. B. msstd:outlook.com *AutoErmittlungsknoten:*  Response/Account/Protocol/CertPrincipalName (EXPR) ) <sup>2</sup> <br/> |
   
### <a name="exchange-2013"></a>Exchange 2013
  
||||
|:-----|:-----|:-----|
|**Eigenschaft** <br/> |**Wert** <br/> |**Beschreibung** <br/> |
|PR_PROFILE_UNRESOLVED_NAME<sup>1</sup> <br/> |Postfachalias  <br/> |Der Alias für das Zielpostfach; z. B. Administrator  <br/> |
|PR_PROFILE_UNRESOLVED_SERVER<sup>1</sup> <br/> |Personalisierte Server-ID  <br/> |Der aus der **AutoErmittlung** abgerufene Wert. im Format <guid> "@tenant.onmicrosoft.com", z. B. F5FA2827-5978-43cd-8FA8-E07BC3BB5591@contoso.onmicrosoft.com  <br/>  *AutoErmittlungsknoten:*  Response/Account/Protocol/Server (EXCH)  <br/> |
|PR_ROH_PROXY_SERVER  <br/> | Domänenname des Clientzugriffsservers  <br/> | Der vollqualifizierte Domänenname (FQDN); beispielsweise e2013cas.contoso.com  *AutoErmittlungsknoten:*  Antwort/Konto/Protokoll/Server (EXPR) <sup>2</sup> <br/> |
|PR_ROH_FLAGS  <br/> |ROHFLAGS_USE_ROH (0x1)  <br/>  ROHFLAGS_HTTP_FIRST_ON_FAST (0x8)  <br/> ROHFLAGS_HTTP_FIRST_ON_SLOW (0x20))  <br/> |Enthält die Einstellungen in einem Profil, das von Outlook zum Herstellen einer Verbindung mit Microsoft Exchange Server mithilfe eines Remoteprozeduraufrufs (RPC) über den *Http-AutoErmittlungsknoten* (Hypertext Transfer Protocol) verwendet wird: Antwort/Konto/Protokoll/SSL (EXPR) <sup>2</sup> <br/> |
| PR_ROH_PROXY_AUTH_SCHEME  <br/> | RPC_C_HTTP_AUTHN_SCHEME_NTLM (0x2)  <br/> |Stellt das Authentifizierungsprotokoll dar, das für diesen *Profil-AutoErmittlungsknoten*  verwendet werden soll: Response/Account/Protocol/AuthPackage (EXPR) <sup>2</sup> <br/> |
|PR_PROFILE_AUTH_PACKAGE  <br/> |RPC_C_AUTHN_WINNT (0xA)  <br/> |Beschreibt das Authentifizierungsschema für RPC *AutoErmittlung Node*  : Response/Account/Protocol/AuthPackage (EXCH) ) <sup>3</sup> <br/> |
   
> [!NOTE] 
> - Alle oben genannten Eigenschaftswerte können für Ihre jeweilige Organisation variieren. 
> - <sup>1</sup> Sie müssen die Unicode-Version anstelle der ANSI-Version verwenden. 
> - Sie müssen die POX-basierte AutoErmittlung (Plain Old XML) verwenden. Dies ist die einzige unterstützte AutoErmittlung zum Konfigurieren von Outlook/Exchange Profilen.
> - Sie können Outlook verwenden, um eine AutoErmittlungsanforderung in Ihrem Namen zu erstellen, indem Sie mit der rechten Maustaste auf das symbol Outlook in der **Taskleiste** des Systems klicken, während Sie STRG gedrückt halten und auf **"Autokonfiguration für E-Mail testen"** klicken. 
> - Für PR_ROH_FLAGS erfordert Ihre Umgebung möglicherweise das Flag ROHFLAGS_SSL_ONLY (0x2), um MAPI anzufordern, nur SSL zu verwenden. Wenn Ihre Umgebung eine gegenseitige Authentifizierung erfordert, müssen Sie dieses Flag auch [ROHFLAGS_MUTUAL_AUTH (0x4)] festlegen. Wenn Sie ROHFLAGS_MUTUAL_AUTH (0x4) festlegen, müssen Sie auch die Eigenschaft PR_ROH_PROXY_PRINCIPAL_NAME festlegen. Sie sollten dies auf den Prinzipalnamen des Servers festlegen.
> - <sup>2</sup> Für Outlook 2010 müssen Sie das EXPR-Protokoll verwenden. Outlook 2013 verwendet das EXHTTP-Protokoll. 
> - <sup>3</sup> Dieser Wert ist möglicherweise nicht in der AutoErmittlungsantwort enthalten. Wenn nicht angegeben, sollte der Client Kerberos oder NTLM verwenden. 
    
Tipps zur Problembehandlung finden Sie unter [Konfigurieren eines Outlook-Profils mit MFCMAPI für Exchange 2013.](https://blogs.msdn.microsoft.com/dvespa/2014/01/16/how-to-configure-an-outlook-profile-using-mfcmapi-for-exchange-2013)
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Referenz für Outlook](https://msdn.microsoft.com/library/office/cc765775.aspx)  
- [Programmgesteuertes Erstellen eines Profils in Outlook](https://msdn.microsoft.com/library/office/mt707568.aspx)
    

