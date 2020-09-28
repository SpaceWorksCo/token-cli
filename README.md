# token-cli

Easily interact with tokens on the SPACE blockchain.

## Using token-cli

```
git clone https://github.com/SpaceWorksCo/token-cli
cd ~/token-cli

# edit spacepath and spacecli if your location differs from spacecoin/src/spacecoin-cli

./token-cli method
```
Please note: anywhere you see `token`, it's looking for the `tokenid` (txid from the token creation). If you wish to use the abbreviation such as `SWTT` (SpaceWorks Test Token) you must add your token to the [token list](https://github.com/SpaceWorksCo/token-cli/blob/master/token-cli#L13).

## Methods

### address

The `address` method returns information about a token address according to a specific pubkey. If no pubkey is provided, the pubkey used to launch the daemon is the default.

`./token-cli address token [pubkey]`

### ask

The `ask` method creates an ask order for the specified token.

`./token-cli ask token numtokens price`

### balance

The `balance` method checks the token balance according to a provided pubkey. If no pubkey is provided, the pubkey used to launch the daemon is the default.

`./token-cli balance token [pubkey]`

### bid

The `bid` method creates a bid order for the specified token.

`./token-cli bid token numtokens price`

### cancelask

The `cancelask` method cancels an existing ask order.

`./token-cli cancelask token asktxid`

### cancelbid

The `cancelbid` method cancels an existing bid order.

`./token-cli cancelbid token bidtxid`

### create

The `create` method creates a new token. For every token created, the method requires one satoshi of SPACE's coins. For example, 1 SPACE provides 100000000 tokens.

The returned txid is your tokenid.

`./token-cli create name supply [description] [data]`

### fillask

The `fillask` method fills an open ask order.

`./token-cli fillask token asktxid fillunits`

### fillbid

The `fillbid` method fills an open bid order.

`./token-cli fillbid token bidtxid fillunits`

### info

The `info` method reveals information about any token.

`./token-cli info token`

### list

The `list` method lists all available tokens on the SPACE chain.

`./token-cli list`

### myorders

The `myorders` method lists all of your token orders on the SPACE chain.

`./token-cli myorders`

### orders

The `orders` method shows the orders for a specified token.

`./token-cli orders token`

### transfer

The `transfer` method sends tokens from one address to another.

`./token-cli transfer token pubkey amount`

## Disclaimer

`token-cli` is a work in progress and subject to change. Please use at your own risk.

## License

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

For details please refer to the [license](https://github.com/SpaceWorksCo/token-cli/blob/master/LICENSE).
