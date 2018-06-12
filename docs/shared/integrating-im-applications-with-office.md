---
title: Integrieren von Chatanwendungen in Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: In diesem Artikel wird beschrieben, wie Sie eine Clientanwendung für Sofortnachrichten konfigurieren, sodass Features für soziale Netzwerke in Office 2013 integriert sind,u. a. Anzeigen von Anwesenheitsinformationen und Senden von Sofortnachrichten von der Visitenkarte aus.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796322"
---
# <a name="integrating-im-applications-with-office"></a>Integrieren von Chatanwendungen in Office

In diesem Artikel wird beschrieben, wie Sie eine Clientanwendung für Sofortnachrichten konfigurieren, sodass Features für soziale Netzwerke in Office 2013 integriert sind,u. a. Anzeigen von Anwesenheitsinformationen und Senden von Sofortnachrichten von der Visitenkarte aus.
  
Wenn Sie Fragen oder Anmerkungen zu diesem technischen Artikel oder zu Prozessen haben, die hier beschrieben werden, können Sie sich direkt per E-Mail unter [docthis@microsoft.com](mailto:docthis@microsoft.com) an Microsoft wenden.
  
## <a name="introduction"></a>Einführung
<a name="off15_IMIntegration_Intro"> </a>

Office 2013 ermöglicht die umfassende Integration mit Clientanwendungen für Chatnachrichten, einschließlich Lync 2013. Diese Integration bietet Benutzern Chat-Funktionen innerhalb von Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 und OneNote 2013 sowie ermöglicht die Anwesenheitsintegration auf SharePoint 2013-Seiten. Benutzer können Foto, Name, Anwesenheitsstatus und Kontaktdaten für Personen in ihrer Kontaktliste sehen. Sie können Chats, Videoanrufe oder Anrufe direkt von der Visitenkarte (das Benutzeroberflächen-Element inOffice 2013 mit Kontaktinformationen und Kommunikationsoptionen) aus durchführen. Office 2013 erleichtert es, mit Kontakten direkt innerhalb von E-Mails oder Dokumenten in Verbindung zu bleiben. 
  
> [!NOTE]
> [!HINWEIS] In diesem Artikel wird der Begriff Clientanwendung für Chatnachrichten verwendet, mit dem speziell die auf dem Benutzercomputer installierte Anwendung gemeint ist, die mit dem Chatdienst kommuniziert. Lync 2013gilt z. B. als eine Clientanwendung für Chatnachrichten. Dieser Artikel enthält keine detaillierten Informationen zur Kommunikation der Clientanwendung für Chatnachrichten mit dem Chatdienst und dem Chatdienst an sich. 
  
Sie können eine Clientanwendung für Chatnachrichten so anpassen, dass diese mit Office kommuniziert. Sie können insbesondere Ihre Chatanwendung zum Anzeigen der folgenden Informationen innerhalb der Office-Benutzeroberfläche anpassen:
  
- Foto des Kontakts
    
- Name des Kontakts
    
- Persönlicher Statushinweis des Kontakts
    
- Anwesenheitsstatus des Kontakts
    
- Zeichenfolge zur Verfügbarkeit des Kontakts (z. B. „Verfügbar" oder „Abwesend").
    
- Zeichenfolge zu unterstützten Chatfunktionen des Kontakts (z. B. „Videomodus möglich").
    
- Chat starten mit einem Klick
    
- Videoanruf starten mit einem Klick
    
- Anruf starten mit einem Klick (SIP, Telefonnummer, Voicemail und neue Anrufnummer)
    
- Kontaktverwaltung (zur Chatgruppe hinzufügen)
    
- Standort und Zeitzone des Kontakts
    
- Kontaktdaten, Telefonnummer, E-Mail-Adresse, Titel und Name des Unternehmens
    
**Abbildung 1. Visitenkarte in Office 2013**

![Die Personenkarte in Office 2013] (media/ocom15_peoplecard.png "Die Personenkarte in Office 2013")
  
Um diese Integration in Office zu ermöglichen, müssen in einer Clientanwendung für Chatnachrichten Schnittstellen implementiert werden, mit denen Office eine Verbindung mit dieser herstellen kann. Die APIs für diese Integration sind im [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx)-Namespace in der Datei „Microsoft.Office.UC.dll" enthalten, die mit Versionen von Office 2013 installiert wird, die Lync/Skype for Business umfassen. Der **UCCollaborationLib**-Namespace enthält die Schnittstellen, die Sie für die Integration in Office implementieren müssen. 
  
> [!IMPORTANT] 
> Die Typbibliothek für die erforderlichen Schnittstellen ist in Lync 2013/Skype für Unternehmen eingebettet. Für Drittanbieterintegratoren funktioniert dies nur, wenn sowohl Lync 2013 als auch Skype for Business auf dem Zielcomputer installiert sind. Wenn Sie die Integration mit Office Standard ausführen, müssen Sie die Typbibliothek extrahieren und auf dem Zielcomputer installieren. Das [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) enthält die Datei Microsoft.Office.UC.dll. 
  
> [!NOTE]
>  [!HINWEIS] Eine Handvoll von Office 2010-Anwendungen können auf ähnliche Weise in einer Drittanbieter-Chatanwendung integriert werden: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 und SharePoint Server 2010 (unter Verwendung eines ActiveX-Steuerelements). Viele der für die Integration in Office 2013 erforderlichen Schritte gelten auch für Office 2010. Es gibt mehrere wichtige Unterschiede bei der Integration von Office 2010 in einer Anwendung des Anbieters für Sofortnachrichten: 
>  - Office 2010 wird das Foto des Kontakts nicht angezeigt. 
>  - Sie müssen die Datei "Microsoft.Office.UC.dll" Datei separat von Office 2010 herunterladen. Das [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) enthält die Datei „Microsoft.Office.UC.dll" für Office 2010. 
>  - Wenn die Office-Anwendung für die Instant Messaging-Client-Anwendung die [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) -Methode aufruft, wird in der Zeichenfolge "14.0.0.0" übergeben. 
>  - Office 2010 Listet alle Gruppen und Kontakte, sobald es mit einer Instant Messaging-Clientanwendung eine Verbindung herstellt. 
  
## <a name="how-office-integrates-with-an-im-client-application"></a>Integration von Office in einer Clientanwendung für Chatnachrichten
<a name="off15_IMIntegration_How"> </a>

Wenn ein Office 2013-Anwendung gestartet wird, durchläuft sie den folgenden Prozess bei der Integration in einer standardmäßigen Clientanwendung für Chatnachrichten:
  
1. Sie prüft die Registrierung, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln, und stellt dann eine Verbindung mit dieser her.
    
2. Sie authentifiziert die Clientanwendung für Chatnachrichten.
    
3. Sie stellt eine Verbindung mit bestimmten Schnittstellen her, die von der Clientanwendung für Chatnachrichten bereitgestellt werden.
    
4. Sie ermittelt die von dem aktuell angemeldeten (lokalen) Benutzer unterstützte Funktionen, u. a. Kontakte des Benutzers, Anwesenheitsinformationen und unterstützte Chatfunktionen (Chatnachrichten, Videoanrufe, VOIP usw.).
    
5. Sie ruft Anwesenheitsinformationen für die Kontakte des lokalen Benutzers ab.
    
6. Wenn die Clientanwendung für Chatnachrichten beendet wird, wird die Verbindung mit der Office 2013-Anwendung im Hintergrund getrennt.
    
### <a name="discovering-the-im-application"></a>Ermitteln der Chatanwendung

Die Office-Anwendung sucht nach bestimmten Schlüsseln und Einträge in der Registrierung, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln. Wenn eine standardmäßigen Clientanwendung für Chatnachrichten festgestellt wird, versucht die Anwendung eine Verbindung mit dieser herzustellen.
  
Der Prozess, den die Office-Anwendung durchläuft, um die standardmäßige Clientanwendung für Chatnachrichten zu ermitteln, ist der folgendende:
  
1. Die Office-Anwendung prüft, ob der Unterschlüssel „HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp" in der Registrierung festgelegt ist, und liest den dort aufgeführten Anwendungsnamen.
    
2. Anschließend liest die Office-Anwendung den Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" Schlüssel und prüft den Wert auf Änderungen.
    
3. Als nächstes liest die Office-Anwendung den Registrierungsschlüssel „HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_" und ruft die dort gespeicherten ProcessName- und Klassen-ID (CLSID)-Werte ab. 
    
4. Sobald die Clientanwendung für Chatnachrichten ihre Startsequenz erfolgreich abgeschlossen und alle Klassen für die Anwesenheitsintegration ordnungsgemäß registriert hat, legt sie den Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" auf den Wert „2" fest, der angibt, dass die Clientanwendung ausgeführt wird.
    
5. Wenn die Office-Anwendung feststellt, dass der Schlüssel „HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning" auf den Wert „2" festgelegt wurde, prüft sie die Liste der ausgeführten Prozesse auf dem Computer auf den Prozessnamen der Clientanwendung für Chatnachrichten.
    
6. Findet die Office-Anwendung den von der Clientanwendung für Chatnachrichten verwendeten Prozess, ruft die Office-Anwendung mit der CLSID **CoCreateInstance** auf, um eine Verbindung mit der Clientanwendung für Chatnachrichten als COM-Server ohne Prozesse herzustellen. 
    
### <a name="authenticating-the-connection-to-the-im-application"></a>Authentifizieren der Verbindung mit der Chatanwendung

Nachdem die Office-Anwendung eine Verbindung mit der Clientanwendung für Chatnachrichten hergestellt hat, führt sie die folgenden Schritte aus:
  
1. Die Office-Anwendung ruft die [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx)-Methode auf, um nach der [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)-Schnittstelle zu suchen. 
    
2. Anschließend ruft die Office-Anwendung die **IUCOfficeIntegration.GetAuthenticationInfo**-Methode auf und übergibt die höchste unterstützte Integrationsversion (z. B. „15.0.0.0"). 
    
3. Wenn die als Parameter übergebene Office-Version von der Clientanwendung für Chatnachrichten unterstützt wird, gibt die Anwendung die folgende hartcodierte XML-Zeichenfolge an den aufrufenden Code zurück:
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > [!HINWEIS] Aufgrund der Kompatibilität mit Vorversionen muss die Clientanwendung für Chatnachrichten den exakten Wert „ `<authenticationinfo>`" für den Aufruf von **GetAuthenticationInfo** zurückgeben, wenn die als Parameter übergebene Office-Version von dieser Anwendung unterstützt wird. 
  
4. Tritt beim Zurückgeben eines Werts durch die Clientanwendung für Chatnachrichten ein Fehler auf, ruft die Office-Anwendung erneut die **GetAuthenticationInfo**-Methode mit der nächsten höchsten unterstützten Version von Office (z. B. „14.0.0.0") auf. 
    
5. Nachdem Office festgestellt hat, dass die Chat- und Anwesenheitsintegration von der Clientanwendung für Chatnachrichten unterstützt wird, stellt es eine Verbindung mit den erforderlichen Schnittstellen her, um die Initialisierung abzuschließen. (Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit den erforderlichen Schnittstellen](#off15_IMIntegration_HowConnect).)
    
Stellt die Office-Anwendung in einem der oben genannten Schritte einen Fehler fest, zieht sie sich zurück, und die Anwensenheitsintegration wird während der Sitzung der Office-Anwendung nicht erneut eingerichtet. 
  
### <a name="connecting-to-required-interfaces"></a>Herstellen einer Verbindung mit den erforderlichen Schnittstellen
<a name="off15_IMIntegration_HowConnect"> </a>

Die Office-Anwendung versucht nach der Authentifizierung der Verbindung mit der Clientanwendung für Chatnachrichten, eine Verbindung mit den erforderlichen Schnittstellen herzustellen, die von der Clientanwendung für Chatnachrichten offen gelegt werden müssen. Dazu führt die Office-Anwendung die folgenden Aktionen durch:
  
- Die Office-Anwendung ruft ein [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)-Objekt durch Aufrufen der **IUCOfficeIntegration.GetInterface**-Methode und Übergeben der **oiInterfaceLyncClient**-Konstante aus der [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface)-Enumeration. 
    
- Die Office-Anwendung ruft ein [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)-Objekt durch Aufrufen der **IUCOfficeIntegration.GetInterface**-Methode und Übergeben der **oiInterfaceAutomation**-Konstante aus der **OIInterface**-Enumeration. 
    
- Die Office-Anwendung richtet den [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)-Ereignislistener ein. 
    
- Die Office-Anwendung richtet den [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)-Ereignislistener ein. 
    
- Die Office-Anwendung ruft den Anmeldestatus aus der Clientanwendung für Chatnachrichten ab, indem sie auf die **ILyncClient.State**-Eigenschaft zugreift. 
    
- Die Office-Anwendung ruft die Funktionen der Clientanwendung für Chantnachrichten durch Aufrufen der **IUCOfficeIntegration.GetSupportedFeatures**-Methode auf, die eine Kennzeichnung aus der [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature)-Enumeration zurückgibt. 
    
- Die Office-Anwendung greift auf die **ILyncClient.Self**-Eigenschaft zu, um einen Verweis auf ein [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf)-Objekt abzurufen. 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a>Abrufen der Funktionen des lokalen Benutzers
<a name="off15_IMIntegration_HowConnect"> </a>

Die Office-Anwendung ruft mithilfe der folgenden Schritte die Funktionen des lokalen Benutzers ab:
  
1. Wenn die Clientanwendung für Chatnachrichten die **IClient2**-Schnittstelle unterstützt, versucht Office ein [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)-Objekt abzurufen, indem es auf die **IClient2.PrivateContactManager**-Eigenschaft zugreift. 
    
2. Wird die **IClient2**-Schnittstelle von der Chatanwendung nicht unterstützt, ruft die Office-Anwendung ein **IContactManager**-Objekt ab, indem es auf die **ILyncClient.ContactManager**-Eigenschaft zugreift. Die Clientanwendung für Chatnachrichten muss erfolgreich ein **IContactManager**-Objekt zurückgeben, bevor andere Chatfunktionen eingerichtet werden können. 
    
3. Die Office-Anwendung greift auf die **ILyncClient.Uri**-Eigenschaft zu und ruft dann **IContactManager.GetContactByUri** auf, um das dem lokalen Benutzer zugewiesene [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact)-Objekt abzurufen. 
    
4. Anschließend führt die Office-Anwendung mehrere Aufrufe von **IContact.CanStart** durch, um die Funktionen des lokalen Benutzers einzurichten, indem die Werte für **ModalityTypes.ucModalityInstantMessage** und **ModalityTypes.ucModalityAudioVideo** nacheinander übergeben werden. 
    
### <a name="retrieving-contact-presence"></a>Abrufen von Anwesenheitsinformationen des Kontakts
<a name="off15_IMIntegration_HowConnect"> </a>

Die Office-Anwendung ruft mithilfe der folgenden Schritte die Anwesenheitsinformationen des Kontakts ab, einschließlich des lokalen Benutzers: 
  
1. Die Office-Anwendung ruft **IContact.GetContactInformation** auf, um ein Anwesenheitselement des Kontakts abzurufen. 
    
2. Anschließend abonniert die Office-Anwendung Änderungen des Anwesenheitsstatus des Kontakts. Sie ruft **IContactManager.CreateSubscription** auf, um ein [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription)-Objekt abzurufen. Als nächstes ruft sie **IContactSubscription.AddContact** zum Hinzufügen des Kontakts zum Abonnement auf und ruft dann **IContactSubscription.Subscribe** auf, um Statusänderungen des Kontakts abzurufen. 
    
3. Wenn die Chatanwendung **IContact2** unterstützt, versucht Office Anwesenheitsinformationen durch Aufrufen von **IContact2.BatchGetContactInformation2**abzurufen.
    
4. Anschließend ruft die Office-Anwendung die Anwesenheitseigenschaften des Kontakts durch Aufrufen von **IContact.BatchGetContactInformation** ab. Die Office-Anwendung kann einen zweiten Satz Anwesenheitseigenschaften durch Zugriff auf die **IContact.Settings**-Eigenschaft abrufen. 
    
5. Abschließend ruft die Office-Anwendung die Gruppenmitgliedschaft des Kontakts ab, indem Sie auf die **IContact.CustomGroups**-Eigenschaft zugreift. Dabei wird eine [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Sammlung mit allen [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Objekten zurückgegeben, bei denen der Kontakt Mitglied ist. 
    
### <a name="disconnecting-from-the-im-application"></a>Trennen der Verbindung mit einer Chatanwendung
<a name="off15_IMIntegration_HowConnect"> </a>

Wenn die Office 2013-Anwendung das **OnShuttingDown**-Ereignis in der Chatanwendung feststellt, wird die Verbindung im Hintergrund getrennt. Wenn die Office-Anwendung vor der Chatanwendung beendet wird, kann die Office-Anwendung jedoch nicht gewährleisten, dass die Verbindung bereinigt wird. Die Chatanwendung muss Verluste der Clientverbindung verarbeiten. 
  
## <a name="setting-registry-keys-and-entries"></a>Festlegen der Registrierungsschlüssel und-Einträge
<a name="off15_IMIntegration_SetRegistry"> </a>

Wie bereits erwähnt, suchen Chat-fähige Office 2013-Anwendungen nach bestimmten Schlüsseln, Einträgen und Werten in der Registrierung, um die Clientanwendung für Chatnachrichten zu ermitteln, mit der eine Verbindung hergestellt werden soll. Diese Registrierungswerte stellen der Office-Anwendung den Prozessnamen und die CLSID der Klasse bereit, die als Einstiegspunkt des Objektmodells der Clientanwendung für Chatnachrichten dient (d. h. die Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert). Die Office-Anwendung ist an der Erstellung dieser Klasse beteiligt und stellt als Client eine Verbindung mit dem COM-Server ohne Prozesse in der Clientanwendung für Chatnachrichten her. 
  
Anhand der Tabelle 1 können Sie Schlüssel, Einträge und Werte identifizieren, die in der Registrierung geschrieben werden müssen, um eine Clientanwendung für Chatnachrichten in Office zu integrieren.
  
**Tabelle 1. Registrierungsschlüssel zum Festlegen der standardmäßigen Clientanwendung für Chatnachrichten**

|**Schlüssel**|**Eintrag**|**Type**|**Wert**|**Beispiel**|
|:-----|:-----|:-----|:-----|:-----|
|HKEY_LOCAL_MACHINE\Software\IM Providers\\< Anwendungsname\>  <br/> |FriendlyName  <br/> |REG_SZ  <br/> |Der Name der Drittanbieter-Clientanwendung für Chatnachrichten.  <br/> |Litware IM 2012  <br/> |
||ProcessName  <br/> |REG_SZ  <br/> |Der Prozessname der Drittanbieter-Clientanwendung für Chatnachrichten.  <br/> |litware.exe  <br/> |
||GUID  <br/> |REG_SZ  <br/> |Eine Klassen-ID (CLSID) für den Stamm, eine mizugestaltende Klasse in der Chatanwendung (Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert).  <br/> |(Eine GUID)  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers  <br/> |DefaultIMApp  <br/> |REG_SZ  <br/> |Der Name der Clientanwendung für Chatnachrichten. Dieser muss mit dem Namen auf oberster Ebene des Registrierungsschlüssels (Struktur) in HKEY_LOCAL_MACHINE übereinstimmen.  <br/> |Litware  <br/> |
|HKEY_CURRENT_USER\Software\IM Providers\\<Anwendungsname\>  <br/> |UpAndRunning  <br/> |REG_DWORD  <br/> | Ein ganzzahliger Wert zwischen 0 und 2:  <br/>  0 - Wird ausgeführt  <br/>  1 - Wird gestartet  <br/>  2 - Wird ausgeführt  <br/> <br/>**Hinweis**: der Anwendung Namen Registrierungsschlüssel muss der Wert des Eintrags DefaultIMApp identisch sein.           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a>Implementieren der erforderlichen Schnittstellen für die Integration in Office
<a name="off15_IMIntegration_ImplementRequired"> </a>

Es gibt drei Schnittstellen aus dem **UCCollaborationLib**-Namespace, die vom ausführbaren Programm (oder COM-Server) einer Clientanwendung für Chatnachrichten für die Integration in Office implementiert werden müssen. Werden diese Schnittstellen nicht implementiert, zieht sich die Office-Anwendung während des Initialisierungsprozesses zurück, und es wird keine Verbindung mit der Clientanwendung für Chatnachrichten hergestellt. 
  
Die erforderlichen Schnittstellen sind die folgenden:
  
- [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration). Die **_IUCOfficeIntegrationEvents**-Schnittstelle sollte, auch wenn nicht erforderlich, auch in der gleichen abgeleiteten Klasse implementiert werden. 
    
- [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient). Die **_ILyncClientEvents**-Schnittstelle sollte, auch wenn nicht erforderlich, auch in der gleichen abgeleiteten Klasse implementiert werden. 
    
- [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a>IUCOfficeIntegration-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a>

Die **IUCOfficeIntegration**-Schnittstelle stellt den Einstiegspunkt für eine Office-Anwendung bereit, um eine Verbindung mit der Clientanwendung für Chatnachrichten herzustellen. Die Schnittstelle definiert drei Methoden, die eine Office-Anwendung im Rahmen der Initialisierung einer Verbindung mit der Clientanwendung für Chatnachrichten aufruft. Die Klasse, die die **IUCOfficeIntegration**-Schnittstelle implementiert, muss eine gemeinsam zu erstellende Klasse sein, damit Office eine Instanz von dieser mitgestalten kann. Darüber hinaus muss sie die CLSID offen legen, die als Wert für den GUID-Eintrag im Registrierungsschlüssel „HKEY_LOCAL_MACHINE\Software\IM Providers\ eingegeben haben, ist _Application name_" eingegeben wird. 
  
Die Klasse, die von **IUCOfficeIntegration** erbt, sollte auch die **_IUCOfficeIntegrationEvents**-Schnittstelle implementieren. Die **_IUCOfficeIntegrationEvents**-Schnittstelle enthält die Elemente, die die Ereignishandler der **IUCOfficeIntegration**-Schnittstelle verfügbar macht. 
  
In Tabelle 2 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IUCOfficeIntegration** und **_IUCOfficeIntegration** erbt.
  
> [!NOTE]
> [!HINWEIS] Weitere Informationen zu den **IUCOfficeIntegration**- und **_IUCOfficeIntegrationEvents**-Schnittstellen und den dazugehörigen Elemente finden Sie unter [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) und [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents). 
  
**Tabelle 2 Implementierung der IUCOfficeIntegration- und _IUCOfficeIntegrationEvents-Schnittstellen**

|**Schnittstelle**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**IUCOfficeIntegration** <br/> |**GetAuthenticationInfo**-Methode  <br/> |Ruft die Zeichenfolge mit den Authentifizierungsinformationen ab.  <br/> |
||**GetInterface**-Methode  <br/> |Ruft die Schnittstelle einer bestimmten Version ab.  <br/> |
||**GetSupportedFeatures**-Methode  <br/> |Ruft die unterstützten Features der Office-Integration ab.  <br/> |
|**_IUCOfficeIntegrationEvents** <br/> |**OnShuttingDown**-Ereignis  <br/> |Das Ereignis, das ausgelöst wird, wenn die Clientanwendung für Chatnachrichten beendet wird.  <br/> |
   
Verwenden Sie den folgenden Code zum Definieren einer Klasse, die von den **IUCOfficeIntegration**- und **_IUCOfficeIntegration**-Schnittstellen innerhalb einer Clientanwendung für Chatnachrichten erbt. 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

Die **GetAuthenticationInfo** -Methode akzeptiert eine Zeichenfolge als Argument für den Parameter _Version_ . Wenn die Office-Anwendung dieser Methode aufruft, übergibt sie eine von zwei Zeichenfolgen für das Argument, je nach der Version von Office. Wenn die Office-Anwendung stellt die Methode mit der Version von Office, die die Instant Messaging-Client-Anwendung unterstützt (d. h., unterstützt die Funktionalität), die **GetAuthenticationInfo** -Methode gibt eine XML-Zeichenfolge hartcodierte `<authenticationinfo>`. 
  
Verwenden Sie den folgenden Code zum Implementieren der **GetAuthentication**-Methode innerhalb des Codes der Clientanwendung für Chatnachrichten. 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

Die **GetInterface**-Methode übermittelt Verweise auf Klassen an den aufrufenden Code, je nachdem, was als Argument für den  _interface_-Parameter übergeben wird. Wenn eine Office-Anwendung die **GetInterface**-Methode aufruft, wird einer von zwei Werten für den Schnittstellenparameter übergeben: entweder die **oiInterfaceILyncClient**-Konstante (1) oder die **oiInterfaceIAutomation**-Konstante (2) der [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface)-Enumeration. Übergibt die Office-Anwendung die **oiInterfaceILyncClient**-Konstante, gibt die **GetInterface**-Methode einen Verweis auf eine Klasse zurück, die die **ILyncClient**-Schnittstelle implementiert. Übergibt die Office-Anwendung die **oiInterfaceIAutomation**-Konstante, gibt die **GetInterface**-Methode eine Klasse zurück, die die **IAutomation**-Schnittstelle implementiert. 
  
Verwenden Sie das folgende Codebeispiel zum Implementieren der **GetInterface**-Methode innerhalb des Codes der Clientanwendung für Chatnachrichten. 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

Die **GetSupportedFeatures**-Methode gibt Informationen zu den Chatfunktionen zurück, die von der Clientanwendung für Chatnachrichten unterstützt werden. Sie verwendet eine Zeichenfolge als einzigen Parameter,  _version_. Wenn die Office-Anwendung die **GetSupportFeatures**-Methode aufruft, gibt die Methode einen Wert aus der [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature)-Enumeration zurück. Der zurückgegebene Wert gibt die Funktionen des Chatclients an, wobei jede Funktion der Clientanwendung für Chatnachrichten mit einer Kennzeichnung des Werts für die Office-Anwendung versehen ist. 
  
> [!NOTE]
>  Office 2013-Anwendungen ignorieren die folgenden Konstanten in der **OIFeature** -Enumeration: 
> - **oiFeaturePictures** (2) 
> - **oiFeatureFreeBusyIntegration**
> - **oiFeaturePhoneNormalization**
  
Verwenden Sie das folgende Codebeispiel zum Implementieren der **GetSupportFeatures**-Methode innerhalb des Codes der Clientanwendung für Chatnachrichten. 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a>ILyncClient-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a>

Die **ILyncClient**-Schnittstelle wird den Funktionen der Clientanwendung für Chatnachrichten zugeordnet. Sie legt die Eigenschaften offen, die auf die bei der Anwendung angemeldete Person (der durch die [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf)-Schnittstelle dargestellte lokale Benutzer), den Status der Anwendung, die Liste der Kontakte des lokalen Benutzers verweisen, und viele andere Einstellungen. Wenn versucht wird, eine Verbindung mit der Clientanwendung für Chatnachrichten herzustellen, ruft die Office-Anwendung einen Verweis auf ein Objekt ab, das die **ILyncClient**-Schnittstelle implementiert. Über diesen Verweis kann Office auf viele Funktionen der Clientanwendung für Chatnachrichten zugreifen. 
  
Darüber hinaus sollte die Klasse, die die **ILyncClient**-Schnittstelle Implementiert, auch die **_ILyncClientEvents**-Schnittstelle implementieren. Die **_ILyncClientEvents**-Schnittstelle legt eine Reihe von Ereignissen offen, die für die Überwachung des Status der Clientanwendung für Chatnachrichten erforderlich sind. 
  
In Tabelle 3 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **ILyncClient** und **_ILyncClientEvents** erbt.
  
> [!NOTE]
> Ein beliebiges Element von der **ILyncClient** oder ** \_ILyncClientEvents** Schnittstelle in der Tabelle nicht aufgeführten muss vorhanden sein, jedoch nicht implementiert werden müssen. Elemente, jedoch nicht implementiert vorhanden sind, können **NotImplementedException** auslösen oder **E\_NOTIMPL** Fehler. 
> 
> Weitere Informationen zu den **ILyncClient** und **_ILyncClientEvents** Schnittstellen und deren Member finden Sie unter [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) und [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents). 
  
**Tabelle 3. Implementierung von ILyncClient- und ILyncClientEvents-Schnittstellen**

|**Schnittstelle**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**ILyncClient** <br/> |**ContactManager**-Eigenschaft  <br/> |Ruft den Kontaktgruppenmanager ab.  <br/> |
||**ConversationManager**-Eigenschaft  <br/> |Ruft den Unterhaltungsmanager ab.  <br/> |
||**Self**-Eigenschaft  <br/> |Ruft das **Self**-Objekt ab.  <br/> |
||**SignIn**-Methode  <br/> |Startet den Anmeldeprozess der Clientanwendung für Chatnachrichten mit einer bestimmten Verfügbarkeit.  <br/> |
||**State**-Eigenschaft  <br/> |Ruft den aktuellen Plattformzustand ab.  <br/> |
||**Uri**-Eigenschaft  <br/> |Ruft den URI der Clientanwendung für Chatnachrichten ab.  <br/> |
|**_ILyncClientEvents** <br/> |**OnStateChanged**-Ereignis  <br/> |Wird ausgelöst, wenn sich der Status der Clientanwendung für Chatnachrichten ändert. Dieses Ereignis sollte verarbeitet werden, und die **eventData.NewState**-Eigenschaft abgerufen werden. Das Ereignis wird für alle Prozesse ausgelöst, die an eine Instanz einer Clientanwendung für Chatnachrichten gebunden sind, wenn ein Subsystem in der Anwendung die Statusänderung auslöst.  <br/> |
   
Während des Initialisierungsprozesses greift Office auf die **ILyncClient.State**-Eigenschaft zu. Diese Eigenschaft muss einen Wert aus der [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState)-Enumeration zurückgeben. 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

Die **State**-Eigenschaft speichert den aktuellen Status der Clientanwendung für Chatnachrichten. Sie muss durchgehend während der Clientanwendungssitzung für Chatnachrichten festgelegt und aktualisiert werden. Beim Anmelden, Abmelden oder Beenden der Clientanwendung für Chatnachrichten sollte die **State**-Eigenschaft festgelegt werden. Es empfiehlt sich, diese Eigenschaft in den **ILyncClient.SignIn**- und **ILyncClient.SignOut**-Methoden festzulegen, wie im folgenden Beispiel veranschaulicht. 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

Das folgende Codebeisiel veranschaulicht die Einrichtung des Ereignislisteners mit den Schnittstellen _ **ILyncClientEvents** und _ **IUCOfficeIntegrationEvents**. 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a>IAutomation-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a>

Die **IAutomation**-Schnittstelle automatisiert Funktionen der Clientanwendung für Chatnachrichten. Sie kann zum Starten von Unterhaltungen, Teilnehmen an Konferenzen und Bereitstellen von Erweiterungsfensterkontext verwendet werden. 
  
In Tabelle 4 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IAutomation** erbt.
  
> [!NOTE]
> [!HINWEIS] Elemente der **IAutomation**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben. 
> 
> Weitere Informationen über die Schnittstelle **IAutomation** und seine Member finden Sie unter [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation). 
  
**Tabelle 4. Implementierung der IAutomation-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**StartConversation**-Methode  <br/> |Startet eine Unterhaltung unter Verwendung der angegebenen Unterhaltungsmodalität. Es wird eine Instanz von **IConversationWindow** zurückgegeben.  <br/> |
   
## <a name="implementing-contact-presence-integration"></a>Implementieren der Kontaktanwesenheitsintegration
<a name="off15_IMIntegration_ImplementIMFeatures"> </a>

Neben den drei beschriebenen erforderlichen Schnittstellen gibt es weitere Schnittstellen, die zum Aktivieren der Kontaktanwesenheitsfunktionen in Office wichtig sind. Hierzu gehören die Folgenden:
  
- Die [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact)- oder **IContact2**-Schnittstellen. 
    
- Die [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf)-Schnittstelle. 
    
- Die [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)- und [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager)-Schnittstellen. 
    
- Die [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)- und [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup)-Schnittstellen. 
    
- Die [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription)-Schnittstelle. 
    
- Die [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint)-Schnittstelle. 
    
- Die [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)-Schnittstelle. 
    
### <a name="icontact-interface"></a>IContact-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_IContact"> </a>

Die **IContact**-Schnittstelle stellt einen Benutzer der Clientanwendung für Chatnachrichten dar. Die Schnittstelle legt Anwesenheitsinformationen, verfügbare Modalitäten, Gruppenmitgliedschaften und Kontakttypeigenschaften für einen Benutzer offen. Um eine Unterhaltung mit einem anderen Benutzer zu beginnen, müssen Sie diese Benutzerinstanz von **IContact** angeben.
  
In Tabelle 5 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IContact** erbt.
  
> [!NOTE]
> [!HINWEIS] Elemente der **IContact**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben. 
>
> Weitere Informationen über die Schnittstelle **IContact** und seine Member finden Sie unter [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact). 
  
**Tabelle 5. Implementierung der IContact-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**CanStart**-Methode  <br/> |Gibt **true** zurück, wenn ein bestimmter Typ Modalität für den Kontakt gestartet werden kann.  <br/> |
|**GetContactInformation**-Methode  <br/> |Ruft ein Anwesenheitselement eines veröffentlichten Kontakts ab.  <br/> |
|**BatchGetContactInformation**-Methode  <br/> |Ruft mehrere Anwesenheitselemente eines veröffentlichten Kontakts ab.  <br/> |
|**Settings**-Eigenschaft  <br/> |Ruft eine Sammlung von Kontakteigenschaften ab.  <br/> |
|**CustomGroups**-Eigenschaft  <br/> |Ruft eine Sammlung von Gruppen auf, bei denen der Kontakt Mitglied ist.  <br/> |
   
Während des Initialisierungsprozesses ruft die Office-Anwendung die **IContact.CanStart**-Methode auf, um die Chatfunktionen für den lokalen Benutzer zu ermitteln. Die **CanStart**-Methode verwendet eine Kennzeichnung aus der[UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes)-Enumeration als Argument für den  __modalityTypes_-Parameter. Wenn der aktuelle Benutzer in der angeforderten Modalität einbezogen werden kann (d. h. der Benutzer verfügt über Chatfunktionen, Funktionen für Audio- und Videoanrufe oder Anwendungsfreigebe), gibt die **CanStart**-Methode **true** zurück.
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

Die **GetContactInformation**-Methode ruft Informationen über den Kontakt aus dem **IContact**-Objekt ab. Der aufgerufene Code muss einen Wert aus der [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType)-Enumeration für den  __contactInformationType_-Parameter übergeben, der die abzurufenden Daten angibt. 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

Ähnlich wie **GetContactInformation**ruft die **BatchGetContactInformation**-Methode mehrere Anwesenheitselemente des Kontakts aus dem **IContact**-Objekt ab. Der aufgerufene Code muss ein Array von Werten aus der **ContactInformationType**-Enumeration für den  __contactInformationTypes_-Parameter übergeben. Die Methode gibt ein [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary)-Objekt mit den angeforderten Daten zurück. 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

Die **IContact.Settings**-Eigenschaft gibt ein **IContactSettingDictionary**-Objekt mit den benutzerdefinierte Eigenschaften des Kontakts zurück. 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

Die **IContact.CustomGroups**-Eigenschaft gibt ein **IGroupCollection**-Objekt mit allen Gruppen zurück, bei denen der Kontakt Mitglied ist. 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a>ISelf-Schnittstelle.
<a name="off15_IMIntegration_ImplementRequired_ISelf"> </a>

Während des Initialisierungsprozesses ruft die Office-Anwendung die Daten für den aktuellen Benutzer durch Zugriff auf die **ILyncClient.Self**-Eigenschaft ab, die ein **ISelf**-Objekt zurückgeben muss. Die **ISelf**-Schnittstelle stellt den lokalen, bei der Clientanwendung für Chatnachrichten angemeldeten Benutzer dar. 
  
In Tabelle 6 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **ISelf** erbt.
  
> [!NOTE]
> [!HINWEIS] Elemente der **ISelf**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben. 
  
**Tabelle 6. Implementierung der ISelf-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Contact**-Eigenschaft  <br/> |Ruft das **IContact**-Objekt ab, das mit dem lokalen Benutzer verknüpft ist.  <br/> |
   
Anwesenheitsinformationen, verfügbare Modalitäten, Gruppenmitgliedschaften und Kontakttypeigenschaften für den lokalen Benutzer werden über die **ISelf.Contact**-Eigenschaft verfügbar gemacht (gibt ein **IContact**-Objekt zurück). Während des Initialisierungsprozesses greift die Office-Anwendung auf die **ISelf.Contact**-Eigenschaft zu, um einen Verweis auf die Kontaktinformationen des lokalen Benutzers abzurufen. 
  
Verwenden Sie den folgenden Code zum Definieren einer Klasse, die von der **ISelf**-Schnittstellen erbt, die die **Contact**-Eigenschaft implementiert. 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a>IContactManager- und _IContactManagerEvents-Schnittstellen
<a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a>

Das **IContactManager**-Objekt verwaltet die Kontakte für den lokalen Benutzer, einschließlich der Kontaktinformationen des lokalen Benutzers. Die Office-Anwendung verwendet ein **IContactManager**-Objekt für den Zugriff auf **IContact**-Objekte, die den Kontakten des lokalen Benutzers entsprechen. 
  
In Tabelle 7 werden die Elemente aufgeführt, die in der Klasse implementiert werden müssen, die von **IContactManager** und **_IContactManagerEvents** erbt.
  
> [!NOTE]
> [!HINWEIS] Elemente der **IContactManager**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, jedoch nicht implementiert vorhanden sind, können **NotImplementedException** auslösen oder **E\_NOTIMPL** Fehler. 
>
> Weitere Informationen zu den **IContactManager** und **_IContactManagerEvents** Schnittstellen und deren Member finden Sie unter [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) und [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents). 
  
**Tabelle 7. Implementierung der IContactManager- und _IContactManagerEvents-Schnittstellen**

|**Schnittstelle**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**IContactManager** <br/> |**GetContactByUri**-Methode  <br/> |Sucht oder erstellt eine Instanz des neuen Kontakts mit dem Kontakt-URI.  <br/> |
||**CreateSubscription**-Methode  <br/> |Erstellt ein **ISubscription**-Objekt, das für die Batchverarbeitung von Abonnements oder Abfragen verwendet werden kann.  <br/> |
||**Lookup**-Methode  <br/> |Sucht nach einer Kontakt- oder Verteilergruppe.  <br/> |
|**_IContactManagerEvents** <br/> |**OnGroupAdded**-Ereignis  <br/> |Wird ausgelöst, wenn eine Gruppe zu einer Gruppensammlung hinzugefügt wird. Die aktualisierte Gruppensammlung kann aus der **IContactManager.Groups**-Eigenschaft abgerufen werden.  <br/> |
||**OnGroupRemoved**-Ereignis  <br/> |Wird ausgelöst, wenn eine Gruppe aus einer Gruppensammlung entfernt wird. Die aktualisierte Gruppensammlung kann aus der **IContactManager.Groups**-Eigenschaft abgerufen werden.  <br/> |
||**OnSearchProviderStateChanged**-Ereignis  <br/> |Wird bei Statusänderung des Suchanbieters ausgelöst.  <br/> |
   
Office ruft **IContactManager.GetContactByUri** zum Abrufen von Anwesenheitsinformationen eines Kontakts unter Verwendung der SIP-Adresse des Kontakts auf. Wenn ein Kontakt für eine SIP-Adresse in Active Directory konfiguriert ist, bestimmt Office diese Adresse für einen Kontakt und ruft **GetContactByUri** auf und übergibt die SIP-Adresse des Kontakts für den  __contactUri_-Parameter. 
  
Wenn Office die SIP-Adresse des Kontakts nicht bestimmen kann, ruft es die **IContactManager.Lookup**-Methode auf, um die SIP über den Chatdienst zu finden. In diesem Fall übergibt Office die besten verfügbaren Daten für den Kontakt (z. B. nur die E-Mail-Adresse für den Kontakt). Die **Lookup**-Methode gibt asynchron ein **AsynchronousOperation**-Objekt zurück. Beim Aufrufen des Rückrufs sollte die **Lookup**-Methode neben dem zurückgegebenen URI des Kontakts angeben, ob der Vorgang erfolgreich war oder dabei ein Fehler aufgetreten ist. 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

Die Office-Anwendung muss Anwesenheitsänderungen für einen bestimmten Kontakt abonnieren. Bei einer Änderung des Anwesenheitsstatus des Kontakts sendet der Chatserver eine Benachrichtigung an die Clientanwendung für Chatnachrichten, wodurch die Office-Anwendung ebenfalls benachrichtigt wird. Dazu ruft die Office-Anwendung die **IContactManager.CreateSubscription**-Methode zum Erstellen eines neuen **IContactSubscription**-Objekts für diese Anforderung auf. 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a>IGroup- und IGroupCollection-Schnittstellen
<a name="off15_IMIntegration_ImplementRequired_IGroup"> </a>

Das **IGroup**-Objekt gibt eine Sammlung von Kontakten mit zusätzlichen Eigenschaften zum Identifizieren der Kontaktsammlung unter Verwendung eines kollektiven Gruppennamens an. Ein **IGroupCollection**-Objekt gibt eine Sammlung von **IGroup**-Objekten an, die durch einen lokalen Benutzer und die Clientanwendung für Chatnachrichten definiert werden. Die Office-Anwendung verwendet die **IGroupCollection**- und **IGroup**-Objekte zum Zugreifen auf die Kontakte des lokalen Benutzers. 
  
In Tabelle 9 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IGroup** und **IGroupCollection** in der folgenden Tabelle erben. 
  
> [!NOTE]
> [!HINWEIS] Elemente der **IGroup**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben. 
>
> Weitere Informationen über die **IGroup** und **IGroupCollection** Schnittstellen und ihre Member finden Sie unter [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) und [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection). 
  
**Tabelle 9. Implementierung der IGroup- und IGroupCollection-Schnittstellen**

|**Schnittstelle**|**Element**|**Beschreibung**|
|:-----|:-----|:-----|
|**IGroupCollection** <br/> |**Count**-Eigenschaft  <br/> |Gibt die Anzahl von **IGroup**-Objekten in der Sammlung zurück.  <br/> |
||**Item**-Eigenschaft  <br/> |Gibt das **IGroup**-Objekt an der angegebenen Indexposition in der Sammlung zurück.  <br/> |
|**IGroup** <br/> |**Id**-Eigenschaft  <br/> |Gibt die ID der Gruppe zurück.  <br/> |
   
Wenn die Office-Anwendung die Informationen für den lokalen Benutzer abruft, greift es auf die Gruppenmitgliedschaften des Kontakts (lokaler Benutzer) durch Aufrufen der **IContact.CustomGroups**-Eigenschaft zu, die ein **IGroupCollection**-Objekt zurückgibt. **IGroupCollection** muss ein Array (oder **List**) von **IGroup**-Objekten enthalten. Die Klasse, die von **IGroupCollection** abgeleitet wird, muss eine **Count**-Eigenschaft verfügbar machen, die die Anzahl der Elemente in der Sammlung und eine Indexermethode zurückgibt, **this(int)**, welche ein **IGroup**-Objekt aus der Sammlung zurückgibt. 
  
### <a name="icontactsubscription-interface"></a>IContactSubscription-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a>

Mit der **IContactSubscription**-Schnittstelle können Sie die Kontakte angeben, die Änderungen an Anwesenheitsinformationen erhalten, und die Typen der Anwesenheitsinformationen, die eine Benachrichtigung auslösen. Office-Anwendungen verwenden ein **IContactSubscription**-Objekt zum Registrieren von Änderungen am Anwesenheitsstatus des Kontakts. 
  
In Tabelle 10 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IContactSubscription** erben.
  
> [!NOTE]
> [!HINWEIS] Elemente der **IContactSubscription**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben.
>
> Weitere Informationen über die Schnittstelle **IContactSubscription** und seine Member finden Sie unter [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription). 
  
**Tabelle 10. Implementierung der IContactSubscription-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**AddContact**-Methode  <br/> |Fügt einen Kontakt zum Abonnementobjekt hinzu.  <br/> |
|**Subscribe**-Methode  <br/> |Hilft der Clientanwendung für Chatnachrichten bei der Überwachung der Anwesenheit eines Kontakts.  <br/> |
   
Die **IContactSubscription**-Schnittstelle muss einen Verweis auf alle überwachten **IContact**-Objekte unter Verwendung eines Arrays oder eines **List**-Objekts enthalten. Die **IContactSubscription.AddContact**-Methode fügt ein **IContact**-Objekt für die zugrunde liegende Datenstruktur des **IContactSubscription**-Objekts hinzu und fügt dabei einen neuen Kontakt hinzu, dessen Anwesenheitsänderungen überwacht werden sollen. 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

Mit der **IContactSubscription.Subscribe**-Methode kann eine Clientanwendung für Chatnachrichten auf Beobachter der Anwesenheitsinformationen eines Kontakts zugreifen. Sie können eine Abrufstrategie zum Abrufen der Anwesenheitsinformationen vom Server für die Kontakte verwenden, die die Clientanwendung für Chatnachrichten abonniert hat. Die **Subscribe**-Methode ist nützlich,wenn Anwesenheitsinformationen für Personen außerhalb der Kontaktliste eines Benutzers (z. B. von einem größeren öffentlichen Netzwerk) angefordert werden. 
  
### <a name="icontactendpoint-interface"></a>IContactEndPoint-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a>

Das **IContactEndPoint**-Objekt gibt eine Telefonnummer aus der Sammlung von Telefonnummern eines Kontakts an. 
  
In Tabelle 11 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **IContactEndPoint** erben.
  
> [!NOTE]
> [!HINWEIS] Elemente der **IContactEndPoint**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben.
>
> Weitere Informationen über die Schnittstelle **IContactEndPoint** und seine Member finden Sie unter [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint). 
  
**Tabelle 11. Implementierung der IContactEndPoint-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**DisplayName**-Eigenschaft  <br/> |Ruft die angezeigte Zeichenfolge ab.  <br/> |
|**Type**-Eigenschaft  <br/> |Ruft den Kontaktendpunkttyp ab.  <br/> |
|**Uri**-Eigenschaft  <br/> |Ruft den Kontakt-URI ab.  <br/> |
   
### <a name="ilocalestring-interface"></a>ILocaleString-Schnittstelle
<a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a>

**ILocaleString** ist eine lokalisierte Zeichenfolgenstruktur, die eine lokalisierte Zeichenfolge und die Gebietsschema-ID der Lokalisierung enthält. Die **ILocaleString**-Schnittstelle wird zum Formatieren der benutzerdefinierten Statuszeichenfolge auf der Visitenkarte verwendet. 
  
In Tabelle 12 werden die Elemente aufgeführt, die in den Klassen implementiert werden müssen, die von **ILocaleString** erben.
  
> [!NOTE]
> [!HINWEIS] Elemente der **ILocaleString**-Schnittstelle, die nicht in der Tabelle aufgeführt sind, müssen zwar vorhanden sein, jedoch nicht implementiert werden. Elemente, die vorhanden sind, jedoch nicht implementiert werden, können einen **NotImplementedException**- oder **E_NOTIMPL**-Fehler zurückgeben.
>
> Weitere Informationen über die Schnittstelle **ILocalString** und seine Member finden Sie unter [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString). 
  
**Tabelle 12. Implementierung der ILocaleString-Schnittstelle**

|**Element**|**Beschreibung**|
|:-----|:-----|
|**LocaleId**-Eigenschaft  <br/> |Ruft die Gebietsschema-ID ab.  <br/> |
|**Value**-Eigenschaft  <br/> |Ruft die Zeichenfolge ab.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)-Namespace 
    

