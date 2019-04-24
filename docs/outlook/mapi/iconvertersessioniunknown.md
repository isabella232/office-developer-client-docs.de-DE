---
title: IConverterSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IConverterSession
api_type:
- COM
ms.assetid: 24f7a14a-aa6f-4045-054b-4a7aefef25e4
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 2db55d6318cf02dd131d07b34841922e61605147
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336687"
---
# <a name="iconvertersession--iunknown"></a><span data-ttu-id="6a844-103">IConverterSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a844-103">IConverterSession : IUnknown</span></span>

  
  
<span data-ttu-id="6a844-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a844-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a844-105">Ermöglicht Konvertierungen zwischen MIME-Objekten und MAPI-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="6a844-105">Allows conversions between MIME objects and MAPI messages.</span></span> <span data-ttu-id="6a844-106">Dies kann beim Transportieren von Nachrichten über das Internet hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="6a844-106">This can be useful in transporting messages across the Internet.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6a844-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="6a844-107">Provided by:</span></span>  <br/> |<span data-ttu-id="6a844-108">CLSID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="6a844-108">CLSID_IConverterSession</span></span>  <br/> |
|<span data-ttu-id="6a844-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="6a844-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6a844-110">IID_IConverterSession</span><span class="sxs-lookup"><span data-stu-id="6a844-110">IID_IConverterSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6a844-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="6a844-111">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6a844-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-112">**[SetAdrBook](iconvertersession-setadrbook.md)**</span></span> <br/> |<span data-ttu-id="6a844-113">Gibt ein optionales MAPI-Adressbuch an, das vom MAPI-in-MIME-Konverter verwendet wird, um mehrdeutige Adressen beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="6a844-113">Specifies an optional MAPI Address Book that the MAPI to MIME converter uses to resolve ambiguous addresses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
|<span data-ttu-id="6a844-114">**[SetEncoding](iconvertersession-setencoding.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-114">**[SetEncoding](iconvertersession-setencoding.md)**</span></span> <br/> |<span data-ttu-id="6a844-115">Initialisiert die Codierung, die während der Konvertierung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6a844-115">Initializes the encoding to use during conversion.</span></span>  <br/> |
| <span data-ttu-id="6a844-116">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6a844-116">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a844-117">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="6a844-117">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="6a844-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-118">**[MIMEToMAPI](iconvertersession-mimetomapi.md)**</span></span> <br/> |<span data-ttu-id="6a844-119">Konvertiert einen MIME-Stream in eine MAPI-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="6a844-119">Converts a MIME stream to a MAPI message.</span></span>  <br/> |
|<span data-ttu-id="6a844-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-120">**[MAPIToMIMEStm](iconvertersession-mapitomimestm.md)**</span></span> <br/> |<span data-ttu-id="6a844-121">Konvertiert eine MAPI-Nachricht in einen MIME-Stream.</span><span class="sxs-lookup"><span data-stu-id="6a844-121">Converts a MAPI message to a MIME stream.</span></span>  <br/> |
| <span data-ttu-id="6a844-122">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6a844-122">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a844-123">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="6a844-123">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="6a844-124">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6a844-124">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a844-125">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="6a844-125">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="6a844-126">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6a844-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a844-127">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="6a844-127">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="6a844-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-128">**[SetTextWrapping](iconvertersession-settextwrapping.md)**</span></span> <br/> |<span data-ttu-id="6a844-129">Legt die Breite des Textumbruchs für einen MIME-Stream fest, der vom Konverter in **MAPIToMIMEStm**zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6a844-129">Sets the text wrapping width for a MIME stream that the converter returns in **MAPIToMIMEStm**.</span></span>  <br/> |
|<span data-ttu-id="6a844-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-130">**[SetSaveFormat](iconvertersession-setsaveformat.md)**</span></span> <br/> |<span data-ttu-id="6a844-131">Legt das Format fest, das der Konverter einen MIME-Stream in **MAPIToMIMEStm**zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="6a844-131">Sets the format that the converter returns a MIME stream in **MAPIToMIMEStm**.</span></span>  <br/> |
| <span data-ttu-id="6a844-132">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="6a844-132">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="6a844-133">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="6a844-133">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="6a844-134">**[SetCharSet](iconvertersession-setcharset.md)**</span><span class="sxs-lookup"><span data-stu-id="6a844-134">**[SetCharSet](iconvertersession-setcharset.md)**</span></span> <br/> |<span data-ttu-id="6a844-135">Gibt einen optionalen Zeichensatz an, den der MAPI-in-MIME-Konverter beim Konvertieren einer MAPI-Nachricht in einen MIME-Stream verwendet.</span><span class="sxs-lookup"><span data-stu-id="6a844-135">Specifies an optional character set that the MAPI to MIME converter uses when converting a MAPI message to a MIME stream.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a844-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a844-136">Remarks</span></span>

<span data-ttu-id="6a844-137">Aufrufen \*\*\*\* der setEncoding vor der Verwendung von **MAPIToMIMEStm** für die Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="6a844-137">Call **SetEncoding** before using **MAPIToMIMEStm** to perform conversion.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6a844-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a844-138">See also</span></span>



[<span data-ttu-id="6a844-139">Informationen über die MAPI-MIME-Konvertierungs-API</span><span class="sxs-lookup"><span data-stu-id="6a844-139">About the MAPI-MIME Conversion API</span></span>](about-the-mapi-mime-conversion-api.md)
  
[<span data-ttu-id="6a844-140">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6a844-140">MAPI Constants</span></span>](mapi-constants.md)

