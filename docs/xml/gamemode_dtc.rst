Destroy the Core
==================

Destroy the Coreゲームモードは相手チームのコアと呼ばれるオブジェクトから溶岩を流出させる事が勝利条件です。 コアの中には溶岩が入っており、コア領域の外まで一定以上溶岩が流れ出ると勝利判定になります。

各チームに一つ以上の ``<core>`` ノードが必要です。また、各チームの ``<core>`` ノードはお互いに対応している必要があります。

.. code-block:: xml

	<cores material="obsidian" leak="3">
		<core team="blue"><cuboid min="-5,73,45" max="-3,78,47"/></core>
		<core team="red"><cuboid min="60,73,45" max="62,78,47"/></core>
	</cores>

.. csv-table:: 
    :header: "属性", "説明","値"
    :widths: 15, 10, 20

    "|material|", 	時間経過によるブロック変化を起こすブロックを決めます。, ":doc:`Material </data/material>`"
    "|leak|", 	溶岩の流す長さを指定します。指定した数字以上の流れが発生すると試合が終わります。, "`Number`"

注意事項
--------

* コアは ``material=""`` に指定した素材で完全に囲むようにしてください。
* コアの範囲座標は外郭がすべて収まる範囲を指定してください。

.. |material| replace:: ``material=""``
.. |leak| replace:: ``leak=""``