---
title: IConverterSessionSetAdrBook
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession.SetAdrBook
api_type:
- COM
ms.assetid: d276ab19-17f4-01c7-4b44-b578e631b5fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7645208e6a0256957deb3a71ba3e04ad125a6b61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326894"
---
# <a name="iconvertersessionsetadrbook"></a><span data-ttu-id="5bb9f-103">IConverterSession::SetAdrBook</span><span class="sxs-lookup"><span data-stu-id="5bb9f-103">IConverterSession::SetAdrBook</span></span>

  
  
<span data-ttu-id="5bb9f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bb9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bb9f-105">Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-in-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-105">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>
  
```cpp
HRESULT IConverterSession::SetAdrBook( 
LPADRBOOK pab); 
```

## <a name="parameters"></a><span data-ttu-id="5bb9f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5bb9f-106">Parameters</span></span>

 <span data-ttu-id="5bb9f-107">_PAB_</span><span class="sxs-lookup"><span data-stu-id="5bb9f-107">_pab_</span></span>
  
> <span data-ttu-id="5bb9f-108">in Zeiger auf eine [IAddrBook: IMAPIProp](iaddrbookimapiprop.md) -Schnittstelle, die in der MAPI-zu-MIME-Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-108">[in] Pointer to an [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface to be used in the MAPI to MIME conversion.</span></span> <span data-ttu-id="5bb9f-109">Legen Sie diesen Parameter auf **null** fest, wenn Sie das Adressbuch nicht mehr benötigen; Dadurch wird die Schnittstelle freigegeben und der Konverter wird so zurückgesetzt, dass kein Adressbuch verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-109">Set this parameter to **null** when you no longer need the Address Book; this releases the interface and resets the converter to not using any Address Book.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5bb9f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5bb9f-110">Return value</span></span>

<span data-ttu-id="5bb9f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bb9f-111">S_OK</span></span>
  
> <span data-ttu-id="5bb9f-112">Der Funktionsaufruf ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-112">The function call is successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bb9f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bb9f-113">Remarks</span></span>

<span data-ttu-id="5bb9f-114">Das Konvertieren einer MAPI-Nachricht in einen MIME-Stream erfordert im Allgemeinen keine Anmeldung an einem MAPI-Profil.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-114">Converting a MAPI message to MIME stream generally does not require logging on to a MAPI profile.</span></span> <span data-ttu-id="5bb9f-115">Wenn Sie jedoch ein MAPI-Adressbuch für die Konvertierung angeben, müssen Sie sich an einem Profil anmelden, um das Adressbuch abzurufen.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-115">However, specifying a MAPI Address Book for conversion requires logging on to a profile to obtain the Address Book.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5bb9f-116">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="5bb9f-116">MFCMAPI reference</span></span>

<span data-ttu-id="5bb9f-117">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5bb9f-118">**Datei**</span><span class="sxs-lookup"><span data-stu-id="5bb9f-118">**File**</span></span>|<span data-ttu-id="5bb9f-119">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="5bb9f-119">**Function**</span></span>|<span data-ttu-id="5bb9f-120">**Comment**</span><span class="sxs-lookup"><span data-stu-id="5bb9f-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bb9f-121">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="5bb9f-121">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5bb9f-122">ImportEMLToIMessage</span><span class="sxs-lookup"><span data-stu-id="5bb9f-122">ImportEMLToIMessage</span></span>  <br/> |<span data-ttu-id="5bb9f-123">MFCMAPI verwendet MimeToMAPI, um eine EML-Datei in eine MAPI-Nachricht umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-123">MFCMAPI uses MimeToMAPI to convert an EML file to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="5bb9f-124">MapiMime. cpp</span><span class="sxs-lookup"><span data-stu-id="5bb9f-124">MapiMime.cpp</span></span>  <br/> |<span data-ttu-id="5bb9f-125">ExportIMessageToEML</span><span class="sxs-lookup"><span data-stu-id="5bb9f-125">ExportIMessageToEML</span></span>  <br/> |<span data-ttu-id="5bb9f-126">MFCMAPI verwendet MAPIToMIMEStm, um eine MAPI-Nachricht in eine EML-Datei umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="5bb9f-126">MFCMAPI uses MAPIToMIMEStm to convert a MAPI message to an EML file.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bb9f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bb9f-127">See also</span></span>



[<span data-ttu-id="5bb9f-128">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bb9f-128">IConverterSession : IUnknown</span></span>](iconvertersessioniunknown.md)
  
[<span data-ttu-id="5bb9f-129">IConverterSession::MAPIToMIMEStm</span><span class="sxs-lookup"><span data-stu-id="5bb9f-129">IConverterSession::MAPIToMIMEStm</span></span>](iconvertersession-mapitomimestm.md)
  
[<span data-ttu-id="5bb9f-130">IConverterSession::MIMEToMAPI</span><span class="sxs-lookup"><span data-stu-id="5bb9f-130">IConverterSession::MIMEToMAPI</span></span>](iconvertersession-mimetomapi.md)
  
[<span data-ttu-id="5bb9f-131">IConverterSession::SetCharSet</span><span class="sxs-lookup"><span data-stu-id="5bb9f-131">IConverterSession::SetCharSet</span></span>](iconvertersession-setcharset.md)
  
[<span data-ttu-id="5bb9f-132">IConverterSession::SetEncoding</span><span class="sxs-lookup"><span data-stu-id="5bb9f-132">IConverterSession::SetEncoding</span></span>](iconvertersession-setencoding.md)
  
[<span data-ttu-id="5bb9f-133">IConverterSession::SetSaveFormat</span><span class="sxs-lookup"><span data-stu-id="5bb9f-133">IConverterSession::SetSaveFormat</span></span>](iconvertersession-setsaveformat.md)
  
[<span data-ttu-id="5bb9f-134">IConverterSession::SetTextWrapping</span><span class="sxs-lookup"><span data-stu-id="5bb9f-134">IConverterSession::SetTextWrapping</span></span>](iconvertersession-settextwrapping.md)

