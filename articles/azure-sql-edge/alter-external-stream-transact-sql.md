---
title: ALTER EXTERNAL STREAM (Transact-SQL) - Azure SQL Edge (プレビュー)
description: Azure SQL Edge での ALTER EXTERNAL STREAM ステートメントについて学習します (プレビュー)
keywords: ''
services: sql-database-edge
ms.service: sql-database-edge
ms.topic: conceptual
author: SQLSourabh
ms.author: sourabha
ms.reviewer: sstein
ms.date: 05/19/2020
ms.openlocfilehash: 0183972b5eb92d3f081b857940609bffc183b331
ms.sourcegitcommit: bb0afd0df5563cc53f76a642fd8fc709e366568b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/19/2020
ms.locfileid: "83595411"
---
# <a name="alter-external-stream-transact-sql"></a>ALTER EXTERNAL STREAM (Transact-SQL)

外部ストリームの定義を変更します。 "*実行中*" 状態のストリーミング ジョブによって使用されている外部ストリームを変更することはできません。 



## <a name="syntax"></a>構文

```sql
  ALTER EXTERNAL STREAM external_stream_name 
  SET 
    [DATA_SOURCE] = <data_source_name> 
    , LOCATION = <location_name> 
    , EXTERNAL_FILE_FORMAT = <external_file_format_name> 
    , INPUT_OPTIONS = <input_options> 
    , OUTPUT_OPTIONS = <output_options> 
```

## <a name="arguments"></a>引数

ALTER EXTERNAL STREAM コマンドの引数の詳細については、「[CREATE EXTERNAL STREAM (Transact-SQL)](create-external-stream-transact-sql.md)」を参照してください。

## <a name="return-code-values"></a>リターン コードの値

成功した場合、ALTER EXTERNAL STREAM は 0 を返します。 0 以外の戻り値は失敗を示します。


## <a name="see-also"></a>関連項目

- [CREATE EXTERNAL STREAM (Transact-SQL)](create-external-stream-transact-sql.md) 
- [DROP EXTERNAL STREAM (Transact-SQL)](drop-external-stream-transact-sql.md) 
