---
title: ISocialSession2LogonCached
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8cac444b-0e81-44ff-a7a0-87793b533e26
description: Meldet sich bei der Website für soziale Netzwerke mithilfe von Anmeldeinformationen.
ms.openlocfilehash: 098ccd2cd3a55affed683886ce1e297ed725475b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796002"
---
# <a name="isocialsession2logoncached"></a><span data-ttu-id="7bc74-103">ISocialSession2::LogonCached</span><span class="sxs-lookup"><span data-stu-id="7bc74-103">ISocialSession2::LogonCached</span></span>

<span data-ttu-id="7bc74-104">Meldet sich bei der Website für soziale Netzwerke mithilfe von Anmeldeinformationen.</span><span class="sxs-lookup"><span data-stu-id="7bc74-104">Logs on to the social network site by using cached credentials.</span></span>
  
```cpp
HRESULT _stdcall LogonCached([in] BSTR connectIn, [in] BSTR userName, [in] BSTR password,  [out] BSTR connectOut);
```

## <a name="parameters"></a><span data-ttu-id="7bc74-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bc74-105">Parameters</span></span>

<span data-ttu-id="7bc74-106">_connectIn_</span><span class="sxs-lookup"><span data-stu-id="7bc74-106">_connectIn_</span></span>
  
> <span data-ttu-id="7bc74-107">[in] Eine Zeichenfolge, die kann leer sein oder enthält die Anmeldeinformationen, je nach den Kontext, in dem die OSC **LogonCached**anruft.</span><span class="sxs-lookup"><span data-stu-id="7bc74-107">[in] A string that can be empty or contains the logon credentials, depending on the context in which the OSC is calling **LogonCached**.</span></span>
    
<span data-ttu-id="7bc74-108">_userName_</span><span class="sxs-lookup"><span data-stu-id="7bc74-108">_userName_</span></span>
  
> <span data-ttu-id="7bc74-109">[in] Eine Zeichenfolge, die den Benutzernamen enthält.</span><span class="sxs-lookup"><span data-stu-id="7bc74-109">[in] A string that contains the user name.</span></span>
    
<span data-ttu-id="7bc74-110">_password_</span><span class="sxs-lookup"><span data-stu-id="7bc74-110">_password_</span></span>
  
> <span data-ttu-id="7bc74-111">[in] Eine Zeichenfolge, die das Kennwort des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="7bc74-111">[in] A string that contains the user's password.</span></span>
    
<span data-ttu-id="7bc74-112">_connectOut_</span><span class="sxs-lookup"><span data-stu-id="7bc74-112">_connectOut_</span></span>
  
> <span data-ttu-id="7bc74-113">[out] Eine opake Zeichenfolge, die Anmeldeinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="7bc74-113">[out] An opaque string that contains credentials.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7bc74-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bc74-114">Remarks</span></span>

<span data-ttu-id="7bc74-115">Diese Methode ist für die Authentifizierung nur aufgerufen, wenn **UseLogonCached** in die **Funktionen** von [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md)zurückgegebenen XML-Daten als **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="7bc74-115">This method is called for authentication only if **useLogonCached** is set as **true** in the **capabilities** XML returned by [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md).</span></span>
  
<span data-ttu-id="7bc74-116">Outlook Social Connector (OSC) **LogonCached**aufruft, und eine leere Zeichenfolge für _ConnectIn_ und nicht leeren Zeichenfolgen für _Benutzername_ und _Kennwort_ übergibt.</span><span class="sxs-lookup"><span data-stu-id="7bc74-116">The Outlook Social Connector (OSC) calls **LogonCached**, and passes an empty string for  _connectIn_ and non-empty  _userName_ and  _password_ strings.</span></span> <span data-ttu-id="7bc74-117">Der Anbieter _Benutzernamen_ und das _Kennwort_ zur Anmeldung bei dem sozialen Netzwerk verwendet und gibt einen undurchsichtiger _ConnectOut_ -Parameter ist die Authentifizierung erfolgreich die OSC zurück.</span><span class="sxs-lookup"><span data-stu-id="7bc74-117">The provider uses  _userName_ and  _password_ to log on to the social network, and returns an opaque  _connectOut_ parameter to the OSC if authentication succeeds.</span></span> <span data-ttu-id="7bc74-118">Wenn Authentifizierung ein Fehler auftritt, gibt der Anbieter den OSC_E_LOGON_FAILURE Fehler an das osc bilden.</span><span class="sxs-lookup"><span data-stu-id="7bc74-118">If authentication fails, the provider returns the OSC_E_LOGON_FAILURE error to the OSC.</span></span> 
  
<span data-ttu-id="7bc74-119">Der Parameter _ConnectOut_ ist eine opake Zeichenfolge an die OSC und auf nachfolgenden Versuche an den Parameter _ConnectIn_ durch die OSC zur Anmeldung bei dem sozialen Netzwerk übergeben.</span><span class="sxs-lookup"><span data-stu-id="7bc74-119">The  _connectOut_ parameter is an opaque string to the OSC, and is passed to the  _connectIn_ parameter on subsequent attempts by the OSC to log on to the social network.</span></span> <span data-ttu-id="7bc74-120">Der Anbieter sollte keine Anmeldeinformationen in der Zeichenfolge _ConnectOut_ platzieren, die der Anbieter das osc bilden, um Verbindungen zu speichern möchte.</span><span class="sxs-lookup"><span data-stu-id="7bc74-120">The provider should place any credentials in the  _connectOut_ string that the provider wants the OSC to store across connections.</span></span> <span data-ttu-id="7bc74-121">Das osc bilden kann nicht die Zeichenfolge in _ConnectOut_interpretieren und verschlüsselt die Zeichenfolge aus Sicherheitsgründen vor dem Speichern in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7bc74-121">The OSC does not interpret the string in  _connectOut_, and encrypts the string for security purposes before storing it in the Windows registry.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7bc74-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bc74-122">See also</span></span>

- [<span data-ttu-id="7bc74-123">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7bc74-123">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

