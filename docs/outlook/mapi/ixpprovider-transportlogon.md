---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 01a8e3c479ab3ddd1be9386e033b993fda5835a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792931"
---
# <a name="ixpprovidertransportlogon"></a><span data-ttu-id="48fbe-103">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="48fbe-103">IXPProvider::TransportLogon</span></span>

<span data-ttu-id="48fbe-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48fbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48fbe-105">Richtet eine Sitzung, in der eine Clientanwendung eines Transportdienstes anmeldet.</span><span class="sxs-lookup"><span data-stu-id="48fbe-105">Establishes a session in which a client application logs on to a transport provider.</span></span> 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a><span data-ttu-id="48fbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="48fbe-106">Parameters</span></span>

<span data-ttu-id="48fbe-107">_LpMAPISup_: [in] Zeiger auf der Adressbuchhierarchie Support-Objekt für Rückruffunktionen in MAPI für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="48fbe-107">_lpMAPISup_: [in] Pointer to the transport provider's support object for callback functions within MAPI for this session.</span></span> <span data-ttu-id="48fbe-108">Dieses Objekt bleibt gültig, bis der Adressbuchhierarchie freigegeben.</span><span class="sxs-lookup"><span data-stu-id="48fbe-108">This object remains valid until the transport provider releases it.</span></span>
    
<span data-ttu-id="48fbe-109">_UlUIParam_: [in] Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows diese Methode zeigt.</span><span class="sxs-lookup"><span data-stu-id="48fbe-109">_ulUIParam_: [in] Handle to the parent window of any dialog boxes or windows this method displays.</span></span> <span data-ttu-id="48fbe-110">Der _UlUIParam_ -Parameter kann nicht Null sein, beispielsweise wenn kennzeichnen der LOGON_SETUP im _LpulFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="48fbe-110">The  _ulUIParam_ parameter can be non-null, for example when the LOGON_SETUP flag is set in the  _lpulFlags_ parameter.</span></span> 
    
<span data-ttu-id="48fbe-111">_LpszProfileName_: [in] Zeiger auf den Profilnamen des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="48fbe-111">_lpszProfileName_: [in] Pointer to the profile name of the user.</span></span> <span data-ttu-id="48fbe-112">Der Parameter _LpszProfileName_ wird hauptsächlich verwendet, wenn ein Dialogfeld angezeigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="48fbe-112">The  _lpszProfileName_ parameter is primarily used when a dialog box must be presented.</span></span> 
    
<span data-ttu-id="48fbe-113">_LpulFlags_: [in, out] Bitmaske aus Flags, die steuert, wie die Sitzung eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="48fbe-113">_lpulFlags_: [in, out] Bitmask of flags that controls how the logon session is established.</span></span> <span data-ttu-id="48fbe-114">Die folgenden Kennzeichen können bei der Eingabe durch die MAPI-Warteschlange festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="48fbe-114">The following flags can be set on input by the MAPI spooler:</span></span>
    
  - <span data-ttu-id="48fbe-115">LOGON_NO_CONNECT: Das Benutzerkonto ist für diesen Transportanbieter für andere Zwecke als Übertragung und Empfang von Nachrichten anmelden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-115">LOGON_NO_CONNECT: The user account is logging on to this transport provider for purposes other than transmission and reception of messages.</span></span> <span data-ttu-id="48fbe-116">Der Transportdienst sollten nicht versuchen, um alle Verbindungen mit anderen messaging-Systemen zu machen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-116">The transport provider should not attempt to make any connections to other messaging systems.</span></span>
        
  - <span data-ttu-id="48fbe-117">LOGON_NO_DIALOG: Kein Dialogfeld sollte angezeigt werden, auch wenn die aktuell gespeicherten Benutzeranmeldeinformationen ungültig oder für die Anmeldung nicht ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="48fbe-117">LOGON_NO_DIALOG: No dialog box should be displayed even if the currently saved user credentials are invalid or insufficient for logon.</span></span>
        
  - <span data-ttu-id="48fbe-118">LOGON_NO_INBOUND: Der Adressbuchhierarchie ist nicht erforderlich, für den Empfang von Nachrichten zu initialisieren und eingehende Nachrichten sollten nicht annehmen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-118">LOGON_NO_INBOUND: The transport provider does not have to initialize for reception of messages and should not accept incoming messages.</span></span> <span data-ttu-id="48fbe-119">Die MAPI-Warteschlange kann später verwenden die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode der Adressbuchhierarchie zum Aktivieren der Verarbeitung der eingehenden Nachricht signalisieren.</span><span class="sxs-lookup"><span data-stu-id="48fbe-119">The MAPI spooler can use the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method later to signal the transport provider to enable incoming message processing.</span></span> 
        
  - <span data-ttu-id="48fbe-120">LOGON_NO_OUTBOUND: Der Adressbuchhierarchie ist nicht erforderlich, initialisieren zum Senden von Nachrichten, die MAPI-Warteschlange eine nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-120">LOGON_NO_OUTBOUND: The transport provider does not have to initialize for sending messages, as the MAPI spooler does not provide any.</span></span> <span data-ttu-id="48fbe-121">Wenn eine Clientanwendung eine Verbindung zu einem remote-Anbieter während der Zusammensetzung des eine Nachricht erforderlich sind, damit es [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufgerufen werden kann, sollte der Adressbuchhierarchie die Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-121">If a client application requires a connection to a remote provider during the composition of a message so that it can make [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method calls, the transport provider should make the connection.</span></span> <span data-ttu-id="48fbe-122">**TransportNotify** können die MAPI-Warteschlange der Adressbuchhierarchie signalisieren, wenn ausgehende Vorgänge beginnen können.</span><span class="sxs-lookup"><span data-stu-id="48fbe-122">The MAPI spooler can use **TransportNotify** to signal the transport provider when outgoing operations can begin.</span></span> 
      
  - <span data-ttu-id="48fbe-123">Parameter MAPI_UNICODE: Die übergebene Zeichenfolge für den Namen des Profils im Unicode-Format ist.</span><span class="sxs-lookup"><span data-stu-id="48fbe-123">MAPI_UNICODE: The passed-in string for the profile name is in Unicode format.</span></span> <span data-ttu-id="48fbe-124">Wenn die MAPI\_Unicode-Flag nicht festgelegt ist, die Zeichenfolge im ANSI-Format ist.</span><span class="sxs-lookup"><span data-stu-id="48fbe-124">If the MAPI\_UNICODE flag is not set, the string is in ANSI format.</span></span>
      
    <span data-ttu-id="48fbe-125">Die folgenden Kennzeichen können bei der Ausgabe von der Adressbuchhierarchie festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="48fbe-125">The following flags can be set on output by the transport provider:</span></span>
      
  - <span data-ttu-id="48fbe-126">LOGON_SP_IDLE: Fordert an, dass die MAPI-Warteschlange leerlaufzeitverarbeitung häufig der Adressbuchhierarchie [IXPLogon::Idle](ixplogon-idle.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-126">LOGON_SP_IDLE: Requests that the MAPI spooler frequently call the transport provider's [IXPLogon::Idle](ixplogon-idle.md) method for idle-time processing.</span></span> 
      
  - <span data-ttu-id="48fbe-127">LOGON_SP_POLL: Anforderungen, die die MAPI-Warteschlange aufrufen häufig die [IXPLogon::Poll](ixplogon-poll.md) -Methode auf das Objekt zurückgegebenen anmelden, um zu überprüfen auf neue Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="48fbe-127">LOGON_SP_POLL: Requests that the MAPI spooler frequently call the [IXPLogon::Poll](ixplogon-poll.md) method on the returned logon object to check for new messages.</span></span> <span data-ttu-id="48fbe-128">Wenn dieses Flag nicht festgelegt ist, überprüft die MAPI-Warteschlange nur für neue Nachrichten, wenn der Adressbuchhierarchie die [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) -Methode verwendet, um der Warteschlange zu benachrichtigen, dass neue Nachrichten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-128">If this flag is not set, the MAPI spooler only checks for new messages when the transport provider uses the [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) method to notify the spooler that there are new messages to process.</span></span> <span data-ttu-id="48fbe-129">Ein Transportdienstes wird effektiv nur senden, indem nicht dieses Flag festlegen und nicht die MAPI-Warteschlange Nachricht Eingang benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-129">A transport provider effectively becomes send-only by not setting this flag and by not notifying the MAPI spooler of message receipt.</span></span> 
      
  - <span data-ttu-id="48fbe-130">LOGON_SP_RESOLVE: Anforderungen, die in die Warteschlange MAPI aufgelöst vollständige Adressen nicht alle Nachrichtenadressen für Empfänger unterstützt von diesem Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="48fbe-130">LOGON_SP_RESOLVE: Requests that the MAPI spooler resolve to full addresses all message addresses for recipients not supported by this transport provider.</span></span> <span data-ttu-id="48fbe-131">Aus diesem Grund, dass der Adressbuchhierarchie für alle Empfänger einen Antwort Pfad erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="48fbe-131">Therefore that the transport provider can construct a reply path for all recipients.</span></span>
      
  - <span data-ttu-id="48fbe-132">Parameter MAPI_UNICODE: Die zurückgegebenen Zeichenfolgen in der Struktur [MAPIERROR](mapierror.md) werden, im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="48fbe-132">MAPI_UNICODE: The returned strings in the [MAPIERROR](mapierror.md) structure, if any, are in Unicode format.</span></span> <span data-ttu-id="48fbe-133">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="48fbe-133">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
<span data-ttu-id="48fbe-134">_LppMAPIError_: [out] Zeiger auf einen Zeiger auf das zurückgegebene **MAPIERROR** -Struktur, sofern zutreffend, enthält Angaben zu Version, Komponente und Kontext für den Fehler.</span><span class="sxs-lookup"><span data-stu-id="48fbe-134">_lppMAPIError_: [out] Pointer to a pointer to the returned **MAPIERROR** structure, if any, that contains version, component, and context information for the error.</span></span> <span data-ttu-id="48fbe-135">Der Parameter _LppMAPIError_ kann auf NULL festgelegt werden, wenn es keine **MAPIERROR** -Struktur ist zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48fbe-135">The  _lppMAPIError_ parameter can be set to NULL if there is no **MAPIERROR** structure to return.</span></span> 
    
<span data-ttu-id="48fbe-136">_LppXPLogon_: [out] Zeiger auf den Zeiger auf das Objekt zurückgegebenen Transport Anbieter anmelden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-136">_lppXPLogon_: [out] Pointer to the pointer to the returned transport provider logon object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48fbe-137">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="48fbe-137">Return value</span></span>

<span data-ttu-id="48fbe-138">S_OK: Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="48fbe-138">S_OK: The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="48fbe-139">MAPI_E_FAILONEPROVIDER: Dieser Anbieter können sich nicht anmelden, aber dieser Fehler sollten Sie den Dienst nicht deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="48fbe-139">MAPI_E_FAILONEPROVIDER: This provider cannot log on, but this error should not disable the service.</span></span> 
    
<span data-ttu-id="48fbe-140">MAPI_E_UNCONFIGURED: Das Profil enthält nicht ausreichend Informationen für die Anmeldung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-140">MAPI_E_UNCONFIGURED: The profile does not contain enough information for the logon to be completed.</span></span> <span data-ttu-id="48fbe-141">MAPI-Aufrufen des Anbieters Nachricht Service Entry Point-Funktion.</span><span class="sxs-lookup"><span data-stu-id="48fbe-141">MAPI calls the provider's message service entry point function.</span></span>
    
<span data-ttu-id="48fbe-142">MAPI_E_UNKNOWN_CPID: Codepage dem Client kann nicht vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-142">MAPI_E_UNKNOWN_CPID: The provider cannot support the client's code page.</span></span>
    
<span data-ttu-id="48fbe-143">MAPI_E_UNKNOWN_LCID: Gebietsschemainformationen der Client kann nicht vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-143">MAPI_E_UNKNOWN_LCID: The provider cannot support the client's locale information.</span></span>
    
<span data-ttu-id="48fbe-144">MAPI_E_USER_CANCEL: Der Benutzer den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="48fbe-144">MAPI_E_USER_CANCEL: The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="48fbe-145">Hinweise</span><span class="sxs-lookup"><span data-stu-id="48fbe-145">Remarks</span></span>

<span data-ttu-id="48fbe-146">Die MAPI-Warteschlange die **IXPProvider::TransportLogon** -Methode aufgerufen, um eine Anmeldung für einen Benutzer einzurichten.</span><span class="sxs-lookup"><span data-stu-id="48fbe-146">The MAPI spooler calls the **IXPProvider::TransportLogon** method to establish a logon session for a user.</span></span> 
  
<span data-ttu-id="48fbe-147">Die meisten Transportanbieter verwenden Sie die [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode mit der Support-Objekt, auf das durch den Parameter _LpMAPISup_ zum Speichern und Abrufen von Benutzeridentitätsinformationen Serveradressen und Anmeldeinformationen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="48fbe-147">Most transport providers use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method provided with the support object pointed to by the  _lpMAPISup_ parameter for saving and retrieving user identity information, server addresses, and credentials.</span></span> <span data-ttu-id="48fbe-148">Mithilfe von **"OpenProfileSection"** kann beliebigen Informationen ein Transportdienstes und versenden eine Anmeldung für eine bestimmte Ressource zuordnen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-148">By using **OpenProfileSection**, a transport provider can save arbitrary information and associate it with a logon to a particular resource.</span></span> <span data-ttu-id="48fbe-149">Beispielsweise können ein Anbieter **"OpenProfileSection"** Sie speichern den Kontonamen und das Kennwort für eine bestimmte Sitzung und keine Servernamen oder andere erforderlichen Informationen, die für diese Sitzung zum Zugriff auf Ressourcen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="48fbe-149">For example, a provider can use **OpenProfileSection** to save the account name and password associated with a particular session and any server names or other necessary information that are required to access resources for that session.</span></span> <span data-ttu-id="48fbe-150">MAPI werden Informationen im Zusammenhang mit einer Ressource außerhalb von Access ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="48fbe-150">MAPI hides information associated with a resource from outside access.</span></span> <span data-ttu-id="48fbe-151">Profilabschnitt über _LpMAPISup_ zur Verfügung gestellt wird durch die MAPI-Warteschlange verwaltet, damit Daten im Zusammenhang mit diesen Benutzerkontext von Daten für andere Kontexte getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="48fbe-151">The profile section made available through  _lpMAPISup_ is managed by the MAPI spooler so data related to this user context is separated from data for other contexts.</span></span> 
  
<span data-ttu-id="48fbe-152">Der Transportdienst muss rufen Sie die **IUnknown:: AddRef** -Methode für das Objekt unterstützt und behalten Sie eine Kopie des Zeigers auf dieses Objekt als Teil des Anbieters Anmeldung-Objekts.</span><span class="sxs-lookup"><span data-stu-id="48fbe-152">The transport provider must call the **IUnknown::AddRef** method on the support object and keep a copy of the pointer to this object as part of the provider logon object.</span></span> 
  
<span data-ttu-id="48fbe-153">Der Anzeigenamen Profil in _LpszProfileName_ wird bereitgestellt, sodass der Adressbuchhierarchie in Fehlermeldungen oder Dialogfelder Anmeldung verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="48fbe-153">The profile display name in  _lpszProfileName_ is provided so the transport provider can use it in error messages or logon dialog boxes.</span></span> <span data-ttu-id="48fbe-154">Wenn der Anbieter dieser Name beibehält, muss er in vom Anbieter reserviert Speicher kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-154">If the provider retains this name, it must be copied to storage allocated by the provider.</span></span> 
  
<span data-ttu-id="48fbe-155">Transportanbieter, die eng mit anderen Dienstanbietern gekoppelt sind möglicherweise zusätzliche Aufgaben bei der Anmeldung die guten für Vorgänge zwischen Anbietern Companion erforderlichen Anmeldeinformationen hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-155">Transport providers that are tightly coupled with other service providers may have to do additional work at logon to establish the good credentials required for operations between companion providers.</span></span>
  
<span data-ttu-id="48fbe-156">In der Regel werden Transportanbieter geöffnet, wenn der Benutzer zuerst zu einem Profil anmeldet.</span><span class="sxs-lookup"><span data-stu-id="48fbe-156">Usually, transport providers are opened when the user first logs on to a profile.</span></span> <span data-ttu-id="48fbe-157">Da die erste Anmeldung zu einem Profil daher im Allgemeinen vor der Anmeldung an alle Nachrichtenspeicher gelangt, ruft die MAPI-Warteschlange **TransportLogon** in der Regel mit der LOGON_NO_INBOUND und die LOGON_NO_OUTBOUND in _LpulFlags_festgelegten Flags.</span><span class="sxs-lookup"><span data-stu-id="48fbe-157">Because the first logon to a profile therefore generally comes before logon to any message store, the MAPI spooler usually calls **TransportLogon** with both the LOGON_NO_INBOUND and LOGON_NO_OUTBOUND flags set in  _lpulFlags_.</span></span> <span data-ttu-id="48fbe-158">Später, wenn die entsprechende Meldung Speicher in der Sitzung Profil verfügbar sind, ruft die MAPI-Warteschlange **TransportNotify** zum ein- und ausgehenden Vorgänge für den Transportanbieter zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="48fbe-158">Later, when the appropriate message stores are available in the profile session, the MAPI spooler calls **TransportNotify** to initiate incoming and outgoing operations for the transport provider.</span></span> 
  
<span data-ttu-id="48fbe-159">Das LOGON_NO_CONNECT-Flag _LpulFlags_ Signale übergeben Offlinebetrieb von der Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="48fbe-159">Passing the LOGON_NO_CONNECT flag in  _lpulFlags_ signals offline operation of the transport provider.</span></span> <span data-ttu-id="48fbe-160">Dieses Kennzeichen gibt an, dass keine externen Verbindungen hergestellt werden soll; Wenn der Adressbuchhierarchie eine Sitzung ohne eine externe Verbindung herstellen kann, muss er einen Fehlerwert für die Anmeldung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="48fbe-160">This flag indicates no external connections should be made; if the transport provider cannot establish a session without an external connection, it should return an error value for the logon.</span></span> 
  
<span data-ttu-id="48fbe-161">Ein Transportdienstes sollte das LOGON_SP_IDLE Flag in _LpulFlags_ bei der Initialisierung festgelegt, wenn es entwickelt wurde, zu verwenden, die das System andernfalls verbringt im Leerlauf.</span><span class="sxs-lookup"><span data-stu-id="48fbe-161">A transport provider should set the LOGON_SP_IDLE flag in  _lpulFlags_ at initialization time if it is designed to use time that the system otherwise spends idle.</span></span> <span data-ttu-id="48fbe-162">So lange wird häufig automatische Vorgänge wie automatische Nachricht herunterladen, ein Timeout aufgetreten Nachricht herunterladen, oder ein Timeout aufgetreten-Nachrichtenübermittlung behandeln.</span><span class="sxs-lookup"><span data-stu-id="48fbe-162">Such time is often used to handle automatic operations, such as automatic message downloading, timed message downloading, or timed message submission.</span></span> <span data-ttu-id="48fbe-163">Wenn dieses Flag festgelegt ist, ruft die MAPI-Warteschlange **im Leerlauf** , wenn im Leerlauf Systemzeit tritt auf, um diese Vorgänge zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="48fbe-163">If this flag is set, the MAPI spooler calls **Idle** when system idle time occurs to initiate such operations.</span></span> <span data-ttu-id="48fbe-164">Die MAPI-Warteschlange wird nicht **im Leerlauf** in festgelegten Intervallen aufgerufen. Stattdessen wird er nur während der Leerlaufzeit true aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-164">The MAPI spooler does not call **Idle** at set intervals; rather, it is called only during true idle time.</span></span> <span data-ttu-id="48fbe-165">Anbieter sollte daher nicht funktionieren, auf alle Annahme darüber, wie häufig ihre Methoden **im Leerlauf** aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-165">Therefore, providers should not work on any assumption about how frequently their **Idle** methods will be called.</span></span> <span data-ttu-id="48fbe-166">Anbieter, die Leerlaufzeit Operationen unterstützen sollte eine Benutzeroberfläche für die Konfiguration dafür in ihren Anbieter-Eigenschaftenfenster bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="48fbe-166">Providers that support idle-time operations should supply a configuration user interface for it in their provider property sheet.</span></span> 
  
<span data-ttu-id="48fbe-167">Wenn die Anmeldung des Transport erfolgreich ist, sollte der Anbieter im _LppXPLogon_ -Parameter einen Zeiger zurückzugeben auf ein Logon-Objekt.</span><span class="sxs-lookup"><span data-stu-id="48fbe-167">If the transport provider logon succeeds, the provider should return in the  _lppXPLogon_ parameter a pointer to a logon object.</span></span> <span data-ttu-id="48fbe-168">Die MAPI-Warteschlange wird dieses Objekt für den Anbieter für zusätzliche Zugriff verwenden.</span><span class="sxs-lookup"><span data-stu-id="48fbe-168">The MAPI spooler will use this object for additional provider access.</span></span> <span data-ttu-id="48fbe-169">Wenn **TransportLogon** das Dialogfeld Anmeldung zeigt und der Benutzer Anmeldung in der Regel abbricht durch Klicken auf die Schaltfläche **Abbrechen** im Dialogfeld sollte der Anbieter MAPI_E_USER_CANCEL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="48fbe-169">If **TransportLogon** displays a logon dialog box and the user cancels logon typically by clicking the **Cancel** button in the dialog box the provider should return MAPI_E_USER_CANCEL.</span></span> 
  
<span data-ttu-id="48fbe-170">Für die meisten Fehlerwerte von **TransportLogon**zurückgegeben deaktiviert MAPI die Message-Dienste zu denen der Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="48fbe-170">For most error values returned from **TransportLogon**, MAPI disables the message services to which the provider belongs.</span></span> <span data-ttu-id="48fbe-171">MAPI rufen keine Anbieter, die zu diesem Dienst für den Rest der MAPI-Sitzung gehören.</span><span class="sxs-lookup"><span data-stu-id="48fbe-171">MAPI will not call any providers that belong to that service for the rest of the MAPI session.</span></span> <span data-ttu-id="48fbe-172">Im Gegensatz dazu gibt **TransportLogon** den Fehlerwert MAPI_E_FAILONEPROVIDER von dessen Anmeldung wird MAPI nicht den Dienst deaktiviert zu dem der Anbieter gehört.</span><span class="sxs-lookup"><span data-stu-id="48fbe-172">In contrast, when **TransportLogon** returns the MAPI_E_FAILONEPROVIDER error value from its logon, MAPI does not disable the message service to which the provider belongs.</span></span> <span data-ttu-id="48fbe-173">**TransportLogon** sollte MAPI_E_FAILONEPROVIDER zurückgegeben, wenn ein Fehler auftritt, der keine Garantie dafür ist das Deaktivieren des Dienstes für den Rest der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="48fbe-173">**TransportLogon** should return MAPI_E_FAILONEPROVIDER if it encounters an error that does not warrant disabling the service for the rest of the session.</span></span> 
  
<span data-ttu-id="48fbe-174">Wenn ein Anbieter von dessen Anmeldung MAPI_E_UNCONFIGURED zurückgibt, wird MAPI Aufrufen des Anbieters Nachricht Service Eintrag-Funktion und wiederholen Sie die Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="48fbe-174">If a provider returns MAPI_E_UNCONFIGURED from its logon, MAPI will call the provider's message service entry function and then retry the logon.</span></span> <span data-ttu-id="48fbe-175">MAPI übergibt MSG_SERVICE_CONFIGURE als Kontext aus, um dem Dienst selbst konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="48fbe-175">MAPI passes MSG_SERVICE_CONFIGURE as the context, to give the service a chance to configure itself.</span></span> <span data-ttu-id="48fbe-176">Wenn der Client sich entschieden hat, um eine Benutzeroberfläche für die Anmeldung zu ermöglichen, kann der Dienst das Eigenschaftenblatt Konfiguration darstellen, damit der Benutzer Informationen eingeben kann.</span><span class="sxs-lookup"><span data-stu-id="48fbe-176">If the client has chosen to allow a user interface on the logon, the service can present its configuration property sheet so that the user can enter configuration information.</span></span> 
  
<span data-ttu-id="48fbe-177">Wenn der Anbieter, dass alle erforderliche Informationen ist nicht im Profil feststellt, sollte MAPI_E_UNCONFIGURED zurückgegeben werden, damit MAPI des Anbieters Nachricht Service Entry Point-Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="48fbe-177">If the provider finds that all the required information is not in the profile, it should return MAPI_E_UNCONFIGURED so that MAPI calls the provider's message service entry point function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48fbe-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="48fbe-178">See also</span></span>

- [<span data-ttu-id="48fbe-179">IXPProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="48fbe-179">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)  
- [<span data-ttu-id="48fbe-180">IMAPISupport::OpenProfileSection</span><span class="sxs-lookup"><span data-stu-id="48fbe-180">IMAPISupport::OpenProfileSection</span></span>](imapisupport-openprofilesection.md)  
- [<span data-ttu-id="48fbe-181">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="48fbe-181">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)  
- [<span data-ttu-id="48fbe-182">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="48fbe-182">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)  
- [<span data-ttu-id="48fbe-183">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="48fbe-183">IXPLogon::Idle</span></span>](ixplogon-idle.md)  
- [<span data-ttu-id="48fbe-184">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="48fbe-184">IXPLogon::Poll</span></span>](ixplogon-poll.md)  
- [<span data-ttu-id="48fbe-185">IXPLogon::TransportNotify</span><span class="sxs-lookup"><span data-stu-id="48fbe-185">IXPLogon::TransportNotify</span></span>](ixplogon-transportnotify.md) 
- [<span data-ttu-id="48fbe-186">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="48fbe-186">MAPIERROR</span></span>](mapierror.md)
