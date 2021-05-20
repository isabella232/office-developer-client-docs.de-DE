---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.
ms.openlocfilehash: b79c692c01022dd10ecb8d4085f0aedb28a810c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436622"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="a2cdd-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="a2cdd-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="a2cdd-104">Meldet sich mit zwischengespeicherten Anmeldeinformationen am Standort des sozialen Netzwerks an.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="a2cdd-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2cdd-105">Parameters</span></span>

<span data-ttu-id="a2cdd-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="a2cdd-106">_connectIn_</span></span>
  
> <span data-ttu-id="a2cdd-107">[in] Eine Zeichenfolge, die leer sein kann oder die Anmeldeinformationen enthält, abhängig vom Kontext, in dem das OSC **LogonCached aufruft.**</span><span class="sxs-lookup"><span data-stu-id="a2cdd-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="a2cdd-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="a2cdd-108">_userName_</span></span>
  
> <span data-ttu-id="a2cdd-109">[in] Eine Zeichenfolge, die den Benutzernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="a2cdd-110">_password_</span><span class="sxs-lookup"><span data-stu-id="a2cdd-110">_password_</span></span>
  
> <span data-ttu-id="a2cdd-111">[in] Eine Zeichenfolge, die das Kennwort des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="a2cdd-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="a2cdd-112">_connectOut_</span></span>
  
> <span data-ttu-id="a2cdd-113">[out] Eine undurchsichtige Zeichenfolge, die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2cdd-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a2cdd-114">Remarks</span></span>

<span data-ttu-id="a2cdd-115">Diese Methode wird nur für die Authentifizierung aufgerufen, wenn  **useLogonCached** in den von ISocialProvider zurückgegebenen Funktionen-XML als **true** festgelegt [ist::GetCapabilities](isocialprovider-getcapabilities.md).</span><span class="sxs-lookup"><span data-stu-id="a2cdd-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="a2cdd-116">Der Outlook Social Connector (OSC) ruft **LogonCached** auf und übergibt eine leere Zeichenfolge für _connectIn-_ und nicht leere _UserName-_ und _Kennwortzeichenfolgen._</span><span class="sxs-lookup"><span data-stu-id="a2cdd-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="a2cdd-117">Der Anbieter verwendet  _userName_ und  _Kennwort,_ um sich beim sozialen Netzwerk zu anmelden, und gibt einen undurchsichtigen  _connectOut-Parameter_ an die OSC zurück, wenn die Authentifizierung erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="a2cdd-118">Wenn bei der Authentifizierung ein Fehler auftritt, gibt der OSC_E_LOGON_FAILURE-Fehler an das Betriebssystem zurück.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="a2cdd-119">Der  _connectOut-Parameter_ ist eine undurchsichtige Zeichenfolge an das OSC und wird bei nachfolgenden Versuchen des OSC, sich beim sozialen Netzwerk zu melden, an den  _connectIn-Parameter_ übergeben.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="a2cdd-120">Der Anbieter sollte alle Anmeldeinformationen in der  _connectOut-Zeichenfolge_ platzieren, die vom Anbieter über verbindungen hinweg vom OSC gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="a2cdd-121">Das OSC interpretiert die Zeichenfolge nicht in _connectOut_ und verschlüsselt die Zeichenfolge aus Sicherheitsgründen, bevor sie in der Windows gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a2cdd-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a2cdd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2cdd-122">See also</span></span>

- [<span data-ttu-id="a2cdd-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2cdd-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

