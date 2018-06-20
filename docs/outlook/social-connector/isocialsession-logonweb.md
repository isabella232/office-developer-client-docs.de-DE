---
title: ISocialSessionLogonWeb
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f4217030-5fd1-4ec4-a83f-752717fbb787
description: Meldet sich bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.
ms.openlocfilehash: 4af0301d5b619ce7f9ff54b97f54b4b00408a564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795995"
---
# <a name="isocialsessionlogonweb"></a><span data-ttu-id="f50df-103">ISocialSession::LogonWeb</span><span class="sxs-lookup"><span data-stu-id="f50df-103">ISocialSession::LogonWeb</span></span>

<span data-ttu-id="f50df-104">Meldet sich bei der Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="f50df-104">Logs on to the social network site by using forms-based authentication.</span></span>
  
```cpp
HRESULT _stdcall LogonWeb([in] BSTR connectIn, [out] BSTR* connectOut);
```

## <a name="parameters"></a><span data-ttu-id="f50df-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="f50df-105">Parameters</span></span>

<span data-ttu-id="f50df-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="f50df-106">_connectIn_</span></span>
  
> <span data-ttu-id="f50df-107">[in] Eine Zeichenfolge, die ist **null**, eine URL zu einem Formular Anmeldung auf dem Web oder eine Zeichenfolge, die Anmeldeinformationen, je nach Kontext während der Anmeldung beim Aufruf dieser Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="f50df-107">[in] A string that is **null**, an URL to a logon form on the web, or a string that contains logon credentials, depending on the context in the logon process when this method is called.</span></span>
    
<span data-ttu-id="f50df-108">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="f50df-108">_connectOut_</span></span>
  
> <span data-ttu-id="f50df-109">[out] Eine Zeichenfolge, die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="f50df-109">[out] A string that contains logon credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f50df-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f50df-110">Remarks</span></span>

<span data-ttu-id="f50df-111">Outlook Social Connector (OSC) Ruft die **LogonWeb** -Methode nur, wenn der Anbieter gibt an, dass sie die formularbasierte Authentifizierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f50df-111">The Outlook Social Connector (OSC) calls the **LogonWeb** method only if the provider indicates that it supports forms-based authentication.</span></span> <span data-ttu-id="f50df-112">Der Anbieter gibt an, dass es formularbasierte Authentifizierung erfordert, indem **UseLogonWebAuth** als **true** in den XML-Code für **Funktionen**festlegen.</span><span class="sxs-lookup"><span data-stu-id="f50df-112">The provider indicates that it requires forms-based authentication by setting **useLogonWebAuth** as **true** in the XML for **capabilities**.</span></span> <span data-ttu-id="f50df-113">Wenn der Anbieter **UseLogonWebAuth** als **false**legt fest, die OSC wird die Standardauthentifizierung verwendet und die [ISocialSession::Logon](isocialsession-logon.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f50df-113">If the provider sets **useLogonWebAuth** as **false**, the OSC uses basic authentication and calls the [ISocialSession::Logon](isocialsession-logon.md) method.</span></span> 
  
<span data-ttu-id="f50df-114">Anmelden bei einer Website für soziale Netzwerke mithilfe der formularbasierten Authentifizierung umfasst das Aufrufen der Methods **LogonWeb** und [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) in einer bestimmten Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="f50df-114">Logging on to a social network site by using forms-based authentication involves calling the **LogonWeb** and [ISocialSession::GetLogonUrl](isocialsession-getlogonurl.md) methods in a specific order:</span></span> 
  
1. <span data-ttu-id="f50df-115">Die OSC ruft **LogonWeb** beim ersten **null** an den _ConnectIn_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f50df-115">The OSC calls **LogonWeb** the first time, passing **null** to the  _connectIn_ parameter.</span></span> 
    
2. <span data-ttu-id="f50df-116">Der Anbieter wird von der OSC_E_AUTH_ERROR Fehler an das osc bilden.</span><span class="sxs-lookup"><span data-stu-id="f50df-116">The provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span>
    
3. <span data-ttu-id="f50df-117">Die OSC-Anrufe Weiter **GetLogonUrl**.</span><span class="sxs-lookup"><span data-stu-id="f50df-117">The OSC next calls **GetLogonUrl**.</span></span>
    
4. <span data-ttu-id="f50df-118">Der Anbieter gibt die entsprechende URL zu einer Anmeldeseite in der **GetLogonUrl** -Methode zurück.</span><span class="sxs-lookup"><span data-stu-id="f50df-118">The provider returns the appropriate URL to a logon page in the **GetLogonUrl** method.</span></span> 
    
5. <span data-ttu-id="f50df-119">Die OSC mithilfe den von **GetLogonUrl** zurückgegebenen URL die Anmeldeseite von formularbasierten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f50df-119">The OSC uses the URL returned by **GetLogonUrl** to display the forms-based logon page.</span></span> 
    
6. <span data-ttu-id="f50df-120">Die OSC ruft dann **LogonWeb** ein zweites Mal die URL an das Anmeldeformular im _ConnectIn_ -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="f50df-120">The OSC then calls **LogonWeb** a second time, passing the URL to the logon form in the  _connectIn_ parameter.</span></span> 
    
7. <span data-ttu-id="f50df-121">Wenn Authentifizierung erfolgreich ist, gibt der Anbieter Anmeldeinformationen im _ConnectOut_ -Parameter an die OSC.</span><span class="sxs-lookup"><span data-stu-id="f50df-121">If authentication succeeds, the provider returns logon credentials in the  _connectOut_ parameter to the OSC.</span></span> <span data-ttu-id="f50df-122">Wenn die Authentifizierung fehlschlägt, löst der Anbieter der OSC_E_AUTH_ERROR Fehler, der die OSC aus.</span><span class="sxs-lookup"><span data-stu-id="f50df-122">If authentication fails, the provider raises the OSC_E_AUTH_ERROR error to the OSC.</span></span> 
    
<span data-ttu-id="f50df-123">Wenn der OSC-Anbieter mit zwischengespeicherten Anmeldeinformationen anmelden unterstützt, gibt **UseLogonCached** in **Funktionen** XML als **true** an.</span><span class="sxs-lookup"><span data-stu-id="f50df-123">If the OSC provider supports logging on using cached credentials, it specifies **useLogonCached** as **true** in the **capabilities** XML.</span></span> <span data-ttu-id="f50df-124">Der Anbieter sollte Anmeldeinformationen in der Zeichenfolge _ConnectOut_ tätigen, die der Anbieter das osc bilden, um Verbindungen zu speichern möchte.</span><span class="sxs-lookup"><span data-stu-id="f50df-124">The provider should place any logon credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="f50df-125">Das osc bilden kann nicht die Zeichenfolge _ConnectOut_ interpretieren.</span><span class="sxs-lookup"><span data-stu-id="f50df-125">The OSC does not interpret the  _connectOut_ string.</span></span> <span data-ttu-id="f50df-126">Nachdem die OSC überprüft hat, dass diese **UseLogonCached** auf **true**festgelegt ist, werden die OSC die Zeichenfolge für die Sicherheit vor dem Speichern in der Windows-Registrierung verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="f50df-126">After the OSC verifies that **useLogonCached** is **true**, the OSC encrypts the string for security before storing it in the Windows registry.</span></span> <span data-ttu-id="f50df-127">Die OSC übergibt diese Zeichenfolge für den Parameter _ConnectIn_ auf nachfolgenden Versuche, die durch Aufrufen von [ISocialSession2::LogonCached](isocialsession2-logoncached.md)in sozialen Netzwerken anmelden.</span><span class="sxs-lookup"><span data-stu-id="f50df-127">The OSC passes this string to the  _connectIn_ parameter on subsequent attempts to log on to the social network by calling [ISocialSession2::LogonCached](isocialsession2-logoncached.md).</span></span> 
  
<span data-ttu-id="f50df-128">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f50df-128">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f50df-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f50df-129">See also</span></span>

- [<span data-ttu-id="f50df-130">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f50df-130">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)
- [<span data-ttu-id="f50df-131">Formularbasierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="f50df-131">Forms-Based Authentication</span></span>](forms-based-authentication.md)

