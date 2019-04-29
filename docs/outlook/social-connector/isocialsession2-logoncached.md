---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen an der Website für soziale Netzwerke an.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436622"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="9d065-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="9d065-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="9d065-104">Meldet sich mithilfe zwischengespeicherter Anmeldeinformationen an der Website für soziale Netzwerke an.</span><span class="sxs-lookup"><span data-stu-id="9d065-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="9d065-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d065-105">Parameters</span></span>

<span data-ttu-id="9d065-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="9d065-106">_connectIn_</span></span>
  
> <span data-ttu-id="9d065-107">in Eine Zeichenfolge, die leer sein oder die Anmeldeinformationen enthalten kann, je nachdem, in welchem Kontext der OSC **LogonCached**aufruft.</span><span class="sxs-lookup"><span data-stu-id="9d065-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="9d065-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="9d065-108">_userName_</span></span>
  
> <span data-ttu-id="9d065-109">in Eine Zeichenfolge, die den Benutzernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="9d065-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="9d065-110">_password_</span><span class="sxs-lookup"><span data-stu-id="9d065-110">_password_</span></span>
  
> <span data-ttu-id="9d065-111">in Eine Zeichenfolge, die das Kennwort des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="9d065-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="9d065-112">_Verbindung_</span><span class="sxs-lookup"><span data-stu-id="9d065-112">_connectOut_</span></span>
  
> <span data-ttu-id="9d065-113">Out Eine undurchsichtige Zeichenfolge, die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="9d065-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d065-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d065-114">Remarks</span></span>

<span data-ttu-id="9d065-115">Diese Methode wird nur für die Authentifizierung aufgerufen, wenn **useLogonCached** in den von [ISocialProvider: getCapabilities](isocialprovider-getcapabilities.md)zurückgegebenen **Capabilities-Funktionen** als **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="9d065-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="9d065-116">Der Outlook Connector für soziale Netzwerke (OSC) ruft **LogonCached**auf und übergibt eine leere Zeichenfolge für _connectin_ und nicht leere _Benutzernamen_ -und _Kenn Wort_ Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="9d065-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="9d065-117">Der Anbieter verwendet _username_ und _Password_ , um sich beim sozialen Netzwerk anzumelden, und gibt einen Opaque- _Verbindungs_ Parameter an den osc zurück, wenn die Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="9d065-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="9d065-118">Wenn die Authentifizierung fehlschlägt, gibt der Anbieter den OSC_E_LOGON_FAILURE-Fehler an den OSC zurück.</span><span class="sxs-lookup"><span data-stu-id="9d065-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="9d065-119">Der __ Parameter Connecting ist eine undurchsichtige Zeichenfolge für OSC und wird bei nachfolgenden Versuchen des osc zur Anmeldung am sozialen Netzwerk an den Parameter _connectin_ übergeben.</span><span class="sxs-lookup"><span data-stu-id="9d065-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="9d065-120">Der Anbieter sollte alle Anmeldeinformationen in der _Verbindungs_ Zeichenfolge platzieren, die der osc über Verbindungen speichern möchte.</span><span class="sxs-lookup"><span data-stu-id="9d065-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="9d065-121">OSC interpretiert die Zeichenfolge nicht in der _Verbindung_und verschlüsselt die Zeichenfolge aus Sicherheitsgründen, bevor Sie in der Windows-Registrierung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9d065-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9d065-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d065-122">See also</span></span>

- [<span data-ttu-id="9d065-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d065-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

