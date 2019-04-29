---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich mithilfe der formularbasierten Authentifizierung an der Website für soziale Netzwerke an.
ms.openlocfilehash: 7ef7af8c1c2cdb783bdecd71b29635468e19dc6a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430336"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="5fe54-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="5fe54-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="5fe54-104">Meldet sich mithilfe der formularbasierten Authentifizierung an der Website für soziale Netzwerke an.</span><span class="sxs-lookup"><span data-stu-id="5fe54-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="5fe54-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5fe54-105">Parameters</span></span>

<span data-ttu-id="5fe54-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="5fe54-106">_connectIn_</span></span>
  
> <span data-ttu-id="5fe54-107">in Eine Zeichenfolge, die **null**ist, eine URL zu einem Anmeldeformular im Web oder eine Zeichenfolge, die Anmeldeinformationen enthält, je nach Kontext im Anmeldeprozess, wenn diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5fe54-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="5fe54-108">_Verbindung_</span><span class="sxs-lookup"><span data-stu-id="5fe54-108">_connectOut_</span></span>
  
> <span data-ttu-id="5fe54-109">Out Eine Zeichenfolge, die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="5fe54-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5fe54-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5fe54-110">Remarks</span></span>

<span data-ttu-id="5fe54-111">Der Outlook Connector für soziale Netzwerke (OSC) Ruft die **LogonWeb** -Methode nur auf, wenn der Anbieter angibt, dass die formularbasierte Authentifizierung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5fe54-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="5fe54-112">Der Anbieter gibt an, dass die formularbasierte Authentifizierung erforderlich ist, indem **useLogonWebAuth** als **true** im XML for **Capabilities**festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="5fe54-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="5fe54-113">Wenn der Anbieter **useLogonWebAuth** als **false**festlegt, verwendet der osc die Standardauthentifizierung und ruft die [ISocialSession:: Login](isocialsession-logon.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="5fe54-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="5fe54-114">Bei der Anmeldung an einem sozialen Netzwerkstandort mithilfe der formularbasierten Authentifizierung müssen Sie die Methoden **LogonWeb** und [ISocialSession:: GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge aufrufen:</span><span class="sxs-lookup"><span data-stu-id="5fe54-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="5fe54-115">OSC ruft **LogonWeb** zum ersten Mal auf und übergibt **null** an den __ Parameter connectin.</span><span class="sxs-lookup"><span data-stu-id="5fe54-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="5fe54-116">Der Anbieter löst den OSC_E_AUTH_ERROR-Fehler an den OSC aus.</span><span class="sxs-lookup"><span data-stu-id="5fe54-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="5fe54-117">Der OSC ruft **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="5fe54-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="5fe54-118">Der Anbieter gibt die entsprechende URL an eine Anmeldeseite in der **GetLogonUrl** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="5fe54-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="5fe54-119">OSC verwendet die von **GetLogonUrl** zurückgegebene URL, um die formularbasierte Anmeldeseite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5fe54-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="5fe54-120">Der OSC ruft dann **LogonWeb** ein zweites Mal auf, wobei die URL an das Anmeldeformular im __ Parameter connectin übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5fe54-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="5fe54-121">Wenn die Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im __ Parameter Connecting an den osc zurück.</span><span class="sxs-lookup"><span data-stu-id="5fe54-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="5fe54-122">Wenn die Authentifizierung fehlschlägt, löst der Anbieter den OSC_E_AUTH_ERROR-Fehler an den OSC aus.</span><span class="sxs-lookup"><span data-stu-id="5fe54-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="5fe54-123">Wenn der OSC-Anbieter die Anmeldung mithilfe zwischengespeicherter Anmeldeinformationen unterstützt, gibt er **useLogonCached** als **true** im **Capabilities** -XML an.</span><span class="sxs-lookup"><span data-stu-id="5fe54-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="5fe54-124">Der Anbieter sollte alle Anmeldeinformationen in der _Verbindungs_ Zeichenfolge platzieren, die der osc über Verbindungen speichern möchte.</span><span class="sxs-lookup"><span data-stu-id="5fe54-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="5fe54-125">OSC interpretiert die _Verbindungs_ Zeichenfolge nicht.</span><span class="sxs-lookup"><span data-stu-id="5fe54-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="5fe54-126">Nachdem OSC überprüft hat, dass **useLogonCached** auf **true**festgelegt ist, verschlüsselt der osc die Zeichenfolge vor dem Speichern in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="5fe54-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="5fe54-127">OSC übergibt diese Zeichenfolge an den __ Parameter connectin bei nachfolgenden Anmeldeversuchen beim sozialen Netzwerk durch Aufrufen von [ISocialSession2:: LogonCached](isocialsession2-logoncached.md).</span><span class="sxs-lookup"><span data-stu-id="5fe54-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="5fe54-128">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5fe54-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5fe54-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fe54-129">See also</span></span>

- [<span data-ttu-id="5fe54-130">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5fe54-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="5fe54-131">Formularbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="5fe54-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

